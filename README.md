namespace CalculatorA
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }
        int locks = 0;
        double first = 0;
        double second = 0;
        double results = 0;
        double n = 0;
        char Ops = ' ';
        string temp = "";
        double holder = 0;
        private void button1_Click(object sender, EventArgs e)
        {
            if (txtScreen.Text == "0")
            {
                txtScreen.Text = "";
            }
            txtScreen.Text += "1";
        }

        private void button0_Click(object sender, EventArgs e)
        {
            if (txtScreen.Text == "0")
            {
                txtScreen.Text = "";
            }
            txtScreen.Text += "0";
        }

        private void button2_Click(object sender, EventArgs e)
        {
            if (txtScreen.Text == "0")
            {
                txtScreen.Text = "";
            }
            txtScreen.Text += "2";
        }

        private void button3_Click(object sender, EventArgs e)
        {
            if (txtScreen.Text == "0")
            {
                txtScreen.Text = "";
            }
            txtScreen.Text += "3";
        }

        private void button4_Click(object sender, EventArgs e)
        {
            if (txtScreen.Text == "0")
            {
                txtScreen.Text = "";
            }
            txtScreen.Text += "4";
        }

        private void button5_Click(object sender, EventArgs e)
        {
            if (txtScreen.Text == "0")
            {
                txtScreen.Text = "";
            }
            txtScreen.Text += "5";
        }

        private void button6_Click(object sender, EventArgs e)
        {
            if (txtScreen.Text == "0")
            {
                txtScreen.Text = "";
            }
            txtScreen.Text += "6";
        }

        private void button7_Click(object sender, EventArgs e)
        {
            if (txtScreen.Text == "0")
            {
                txtScreen.Text = "";
            }
            txtScreen.Text += "7";
        }

        private void button8_Click(object sender, EventArgs e)
        {
            if (txtScreen.Text == "0")
            {
                txtScreen.Text = "";
            }
            txtScreen.Text += "8";
        }

        private void button9_Click(object sender, EventArgs e)
        {
            if (txtScreen.Text == "0")
            {
                txtScreen.Text = "";
            }
            txtScreen.Text += "9";
        }

        private void btnClear_Click(object sender, EventArgs e)
        {
            txtScreen.Text = "0";
        }

        private void btnClearAll_Click(object sender, EventArgs e)
        {
            txtScreen.Text = "0";
            txtSub.Text = "0";
            first = 0;
            second = 0;
            Ops = ' ';
        }

        private void btnMultiply_Click(object sender, EventArgs e)
        {
            if (Ops == 'a'){
                holder = first + second;
                first = holder;
                second = 0;
            }
            if (Ops == 's'){
                holder = first - second;
                first = holder;
                second = 0;
            }
            if (Ops == 'd'){
                holder = first / second;
                first = holder;
                second = 0;
            }
            if (Ops == 'm'){
                holder = first * second;
                first = holder;
                second = 0;
            }

            temp = "";
            Ops = 'm';
            if (txtScreen.Text != "0")
            {
                
                first = double.Parse(txtScreen.Text);
                txtScreen.Text = $"{first}*";
                
                locks--;
            }



        }

        private void btnSubtract_Click(object sender, EventArgs e)
        {
            if (Ops == 'a')
            {
                holder = first + second;
                first = holder;
                second = 0;
            }
            if (Ops == 's')
            {
                holder = first - second;
                first = holder;
                second = 0;
            }
            if (Ops == 'd')
            {
                holder = first / second;
                first = holder;
                second = 0;
            }
            if (Ops == 'm')
            {
                holder = first * second;
                first = holder;
                second = 0;
            }

            temp = "";
            Ops = 's';
            if (txtScreen.Text != "0")
            {
                
                first = double.Parse(txtScreen.Text);
                txtScreen.Text = $"{first}-";
                locks--;
            }


        }

        private void btnAdd_Click(object sender, EventArgs e)
        {

            if (Ops == 'a')
            {
                holder = first + second;
                first = holder;
                second = 0;
            }
            if (Ops == 's')
            {
                holder = first - second;
                first = holder;
                second = 0;
            }
            if (Ops == 'd')
            {
                holder = first / second;
                first = holder;
                second = 0;
            }
            if (Ops == 'm')
            {
                holder = first * second;
                first = holder;
                second = 0;
            }
            temp = "";
            Ops = 'a';
            if (txtScreen.Text != "0")
            {
                

                first = double.Parse(txtScreen.Text);
                txtScreen.Text = $"{first}+";

                locks--;
            }


        }

        private void btnDivide_Click(object sender, EventArgs e)
        {
            if (Ops == 'a')
            {
                holder = first + second;
                first = holder;
                second = 0;
            }
            if (Ops == 's')
            {
                holder = first - second;
                first = holder;
                second = 0;
            }
            if (Ops == 'd')
            {
                holder = first / second;
                first = holder;
                second = 0;
            }
            if (Ops == 'm')
            {
                holder = first * second;
                first = holder;
                second = 0;
            }

            temp = "";
            Ops = 'd';
            if (txtScreen.Text != "0")
            {
                
                first = double.Parse(txtScreen.Text);
               
                txtScreen.Text = $"{first}÷";
                locks--;
            }



        }

        private void btnEqual_Click(object sender, EventArgs e)
        {
            second = double.Parse(txtScreen.Text);
            if (Ops == 'a')
            {
                results = first + second;
                txtSub.Text = $"{first} + {second}";
            }
            if (Ops == 's')
            {
                results = first - second;
                txtSub.Text = $"{first} - {second}";
            }
            if (Ops == 'm')
            {
                results = first * second;
                txtSub.Text = $"{first} * {second}";
            }
            if (Ops == 'd')
            {
                results = first / second;
                txtSub.Text = $"{first} ÷ {second}";
            }
            txtScreen.Text = results + "";

            temp = "";
        }

        private void btnErase_Click(object sender, EventArgs e)
        {
            string txt = txtScreen.Text;
            if (txt.Length > 0)
            {
                txt = txt.Remove(txt.Length - 1);
            }
            txtScreen.Text = txt;
        }

        private void btnDecimal_Click(object sender, EventArgs e)
        {
            if (locks == 0)
            {
                if (txtScreen.Text == "0")
                {
                    txtScreen.Text = "";
                }
                txtScreen.Text += btnDecimal.Text;
                locks++;
            }

        }

        private void btnSign_Click(object sender, EventArgs e)
        {
            n = double.Parse(txtScreen.Text);
            n *= -1;
            txtScreen.Text = n.ToString();
        }
    }
}




namespace CalculatorA
{
    partial class Form1
    {
        /// <summary>
        ///  Required designer variable.
        /// </summary>
        private System.ComponentModel.IContainer components = null;

        /// <summary>
        ///  Clean up any resources being used.
        /// </summary>
        /// <param name="disposing">true if managed resources should be disposed; otherwise, false.</param>
        protected override void Dispose(bool disposing)
        {
            if (disposing && (components != null))
            {
                components.Dispose();
            }
            base.Dispose(disposing);
        }

        #region Windows Form Designer generated code

        /// <summary>
        ///  Required method for Designer support - do not modify
        ///  the contents of this method with the code editor.
        /// </summary>
        private void InitializeComponent()
        {
            button1 = new Button();
            button2 = new Button();
            button3 = new Button();
            button4 = new Button();
            button5 = new Button();
            button6 = new Button();
            button7 = new Button();
            button8 = new Button();
            button9 = new Button();
            btnSign = new Button();
            button0 = new Button();
            btnDecimal = new Button();
            btnClear = new Button();
            btnClearAll = new Button();
            btnMultiply = new Button();
            btnDivide = new Button();
            btnAdd = new Button();
            btnSubtract = new Button();
            btnErase = new Button();
            btnEqual = new Button();
            txtScreen = new TextBox();
            txtSub = new TextBox();
            SuspendLayout();
            // 
            // button1
            // 
            button1.BackgroundImageLayout = ImageLayout.None;
            button1.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            button1.Location = new Point(12, 286);
            button1.Name = "button1";
            button1.Size = new Size(75, 73);
            button1.TabIndex = 0;
            button1.Text = "1";
            button1.UseVisualStyleBackColor = true;
            button1.Click += button1_Click;
            // 
            // button2
            // 
            button2.BackgroundImageLayout = ImageLayout.None;
            button2.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            button2.Location = new Point(93, 286);
            button2.Name = "button2";
            button2.Size = new Size(75, 73);
            button2.TabIndex = 1;
            button2.Text = "2";
            button2.UseVisualStyleBackColor = true;
            button2.Click += button2_Click;
            // 
            // button3
            // 
            button3.BackgroundImageLayout = ImageLayout.None;
            button3.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            button3.Location = new Point(174, 286);
            button3.Name = "button3";
            button3.Size = new Size(75, 73);
            button3.TabIndex = 2;
            button3.Text = "3";
            button3.UseVisualStyleBackColor = true;
            button3.Click += button3_Click;
            // 
            // button4
            // 
            button4.BackgroundImageLayout = ImageLayout.None;
            button4.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            button4.Location = new Point(12, 207);
            button4.Name = "button4";
            button4.Size = new Size(75, 73);
            button4.TabIndex = 3;
            button4.Text = "4";
            button4.UseVisualStyleBackColor = true;
            button4.Click += button4_Click;
            // 
            // button5
            // 
            button5.BackgroundImageLayout = ImageLayout.None;
            button5.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            button5.Location = new Point(93, 207);
            button5.Name = "button5";
            button5.Size = new Size(75, 73);
            button5.TabIndex = 4;
            button5.Text = "5";
            button5.UseVisualStyleBackColor = true;
            button5.Click += button5_Click;
            // 
            // button6
            // 
            button6.BackgroundImageLayout = ImageLayout.None;
            button6.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            button6.Location = new Point(174, 207);
            button6.Name = "button6";
            button6.Size = new Size(75, 73);
            button6.TabIndex = 5;
            button6.Text = "6";
            button6.UseVisualStyleBackColor = true;
            button6.Click += button6_Click;
            // 
            // button7
            // 
            button7.BackgroundImageLayout = ImageLayout.None;
            button7.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            button7.Location = new Point(12, 128);
            button7.Name = "button7";
            button7.Size = new Size(75, 73);
            button7.TabIndex = 6;
            button7.Text = "7";
            button7.UseVisualStyleBackColor = true;
            button7.Click += button7_Click;
            // 
            // button8
            // 
            button8.BackgroundImageLayout = ImageLayout.None;
            button8.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            button8.Location = new Point(93, 128);
            button8.Name = "button8";
            button8.Size = new Size(75, 73);
            button8.TabIndex = 7;
            button8.Text = "8";
            button8.UseVisualStyleBackColor = true;
            button8.Click += button8_Click;
            // 
            // button9
            // 
            button9.BackgroundImageLayout = ImageLayout.None;
            button9.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            button9.Location = new Point(174, 128);
            button9.Name = "button9";
            button9.Size = new Size(75, 73);
            button9.TabIndex = 8;
            button9.Text = "9";
            button9.UseVisualStyleBackColor = true;
            button9.Click += button9_Click;
            // 
            // btnSign
            // 
            btnSign.BackgroundImageLayout = ImageLayout.None;
            btnSign.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            btnSign.Location = new Point(12, 365);
            btnSign.Name = "btnSign";
            btnSign.Size = new Size(75, 73);
            btnSign.TabIndex = 9;
            btnSign.Text = "+/-";
            btnSign.UseVisualStyleBackColor = true;
            btnSign.Click += btnSign_Click;
            // 
            // button0
            // 
            button0.BackgroundImageLayout = ImageLayout.None;
            button0.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            button0.Location = new Point(93, 365);
            button0.Name = "button0";
            button0.Size = new Size(75, 73);
            button0.TabIndex = 10;
            button0.Text = "0";
            button0.UseVisualStyleBackColor = true;
            button0.Click += button0_Click;
            // 
            // btnDecimal
            // 
            btnDecimal.BackgroundImageLayout = ImageLayout.None;
            btnDecimal.Font = new Font("Segoe UI", 24F, FontStyle.Regular, GraphicsUnit.Point);
            btnDecimal.Location = new Point(174, 365);
            btnDecimal.Name = "btnDecimal";
            btnDecimal.Size = new Size(75, 73);
            btnDecimal.TabIndex = 11;
            btnDecimal.Text = ".";
            btnDecimal.UseVisualStyleBackColor = true;
            btnDecimal.Click += btnDecimal_Click;
            // 
            // btnClear
            // 
            btnClear.BackgroundImageLayout = ImageLayout.None;
            btnClear.Font = new Font("Segoe UI", 21.75F, FontStyle.Regular, GraphicsUnit.Point);
            btnClear.Location = new Point(255, 128);
            btnClear.Name = "btnClear";
            btnClear.Size = new Size(75, 73);
            btnClear.TabIndex = 12;
            btnClear.Text = "C";
            btnClear.UseVisualStyleBackColor = true;
            btnClear.Click += btnClear_Click;
            // 
            // btnClearAll
            // 
            btnClearAll.BackgroundImageLayout = ImageLayout.None;
            btnClearAll.Font = new Font("Segoe UI", 21.75F, FontStyle.Regular, GraphicsUnit.Point);
            btnClearAll.Location = new Point(336, 128);
            btnClearAll.Name = "btnClearAll";
            btnClearAll.Size = new Size(75, 73);
            btnClearAll.TabIndex = 13;
            btnClearAll.Text = "CE";
            btnClearAll.UseVisualStyleBackColor = true;
            btnClearAll.Click += btnClearAll_Click;
            // 
            // btnMultiply
            // 
            btnMultiply.BackgroundImageLayout = ImageLayout.None;
            btnMultiply.Font = new Font("Segoe UI", 21.75F, FontStyle.Regular, GraphicsUnit.Point);
            btnMultiply.Location = new Point(255, 207);
            btnMultiply.Name = "btnMultiply";
            btnMultiply.Size = new Size(75, 73);
            btnMultiply.TabIndex = 14;
            btnMultiply.Text = "x";
            btnMultiply.UseVisualStyleBackColor = true;
            btnMultiply.Click += btnMultiply_Click;
            // 
            // btnDivide
            // 
            btnDivide.BackgroundImageLayout = ImageLayout.None;
            btnDivide.Font = new Font("Segoe UI", 21.75F, FontStyle.Regular, GraphicsUnit.Point);
            btnDivide.Location = new Point(336, 286);
            btnDivide.Name = "btnDivide";
            btnDivide.Size = new Size(75, 73);
            btnDivide.TabIndex = 15;
            btnDivide.Text = "÷";
            btnDivide.UseVisualStyleBackColor = true;
            btnDivide.Click += btnDivide_Click;
            // 
            // btnAdd
            // 
            btnAdd.BackgroundImageLayout = ImageLayout.None;
            btnAdd.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            btnAdd.Location = new Point(255, 365);
            btnAdd.Name = "btnAdd";
            btnAdd.Size = new Size(75, 73);
            btnAdd.TabIndex = 16;
            btnAdd.Text = "+";
            btnAdd.UseVisualStyleBackColor = true;
            btnAdd.Click += btnAdd_Click;
            // 
            // btnSubtract
            // 
            btnSubtract.BackgroundImageLayout = ImageLayout.None;
            btnSubtract.Font = new Font("Segoe UI", 24F, FontStyle.Regular, GraphicsUnit.Point);
            btnSubtract.Location = new Point(255, 286);
            btnSubtract.Name = "btnSubtract";
            btnSubtract.Size = new Size(75, 73);
            btnSubtract.TabIndex = 16;
            btnSubtract.Text = "-";
            btnSubtract.UseVisualStyleBackColor = true;
            btnSubtract.Click += btnSubtract_Click;
            // 
            // btnErase
            // 
            btnErase.BackgroundImageLayout = ImageLayout.None;
            btnErase.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            btnErase.Location = new Point(336, 207);
            btnErase.Name = "btnErase";
            btnErase.Size = new Size(75, 73);
            btnErase.TabIndex = 17;
            btnErase.Text = "DEL";
            btnErase.UseVisualStyleBackColor = true;
            btnErase.Click += btnErase_Click;
            // 
            // btnEqual
            // 
            btnEqual.BackgroundImageLayout = ImageLayout.None;
            btnEqual.Font = new Font("Segoe UI", 18F, FontStyle.Regular, GraphicsUnit.Point);
            btnEqual.Location = new Point(336, 365);
            btnEqual.Name = "btnEqual";
            btnEqual.Size = new Size(75, 73);
            btnEqual.TabIndex = 18;
            btnEqual.Text = "=";
            btnEqual.UseVisualStyleBackColor = true;
            btnEqual.Click += btnEqual_Click;
            // 
            // txtScreen
            // 
            txtScreen.Enabled = false;
            txtScreen.Font = new Font("Segoe UI", 36F, FontStyle.Regular, GraphicsUnit.Point);
            txtScreen.ForeColor = SystemColors.WindowText;
            txtScreen.Location = new Point(12, 8);
            txtScreen.Name = "txtScreen";
            txtScreen.Size = new Size(399, 71);
            txtScreen.TabIndex = 19;
            txtScreen.Text = "0";
            txtScreen.TextAlign = HorizontalAlignment.Right;
            // 
            // txtSub
            // 
            txtSub.Enabled = false;
            txtSub.Font = new Font("Segoe UI", 12F, FontStyle.Regular, GraphicsUnit.Point);
            txtSub.Location = new Point(12, 85);
            txtSub.Name = "txtSub";
            txtSub.Size = new Size(399, 29);
            txtSub.TabIndex = 20;
            txtSub.Text = "0";
            txtSub.TextAlign = HorizontalAlignment.Right;
            // 
            // Form1
            // 
            AutoScaleDimensions = new SizeF(7F, 15F);
            AutoScaleMode = AutoScaleMode.Font;
            BackColor = Color.PowderBlue;
            ClientSize = new Size(423, 450);
            Controls.Add(txtSub);
            Controls.Add(txtScreen);
            Controls.Add(btnEqual);
            Controls.Add(btnErase);
            Controls.Add(btnSubtract);
            Controls.Add(btnAdd);
            Controls.Add(btnDivide);
            Controls.Add(btnMultiply);
            Controls.Add(btnClearAll);
            Controls.Add(btnClear);
            Controls.Add(btnDecimal);
            Controls.Add(button0);
            Controls.Add(btnSign);
            Controls.Add(button9);
            Controls.Add(button8);
            Controls.Add(button7);
            Controls.Add(button6);
            Controls.Add(button5);
            Controls.Add(button4);
            Controls.Add(button3);
            Controls.Add(button2);
            Controls.Add(button1);
            Name = "Form1";
            Text = "Form1";
            Load += Form1_Load;
            ResumeLayout(false);
            PerformLayout();
        }

        #endregion

        private Button button1;
        private Button button2;
        private Button button3;
        private Button button4;
        private Button button5;
        private Button button6;
        private Button button7;
        private Button button8;
        private Button button9;
        private Button btnSign;
        private Button button0;
        private Button btnDecimal;
        private Button btnClear;
        private Button btnClearAll;
        private Button btnMultiply;
        private Button btnDivide;
        private Button btnAdd;
        private Button btnSubtract;
        private Button btnErase;
        private Button btnEqual;
        private TextBox txtScreen;
        private TextBox txtSub;
    }
}
