# Week-4---7-Programming
Week 4 - 7 Programming Code


using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Section2Week4_7Project
{
    public partial class frmBinary : Form
    {
        public frmBinary()
        {
            InitializeComponent();
        }

        private void Convert(int first)
        {
            int x = first;
            decimal dInt = 0.0m;
            string integer = textBox1.Text;
            dInt = System.Convert.ToInt32(integer);
            int remainder;
            string result = string.Empty;
            while (dInt > 0)
            {
                remainder = (int)(dInt % 2);
                dInt /= x;
                result = remainder.ToString() + result;

            }
            label1.Text = result;
        }

        private void txtBox1Convert_TextChanged(object sender, EventArgs e)
        {

        }

        private void txtBox2Base_TextChanged(object sender, EventArgs e)
        {

        }

        private void lbl1Message_Click(object sender, EventArgs e)
        {

        }

        private void btnClear_Click(object sender, EventArgs e)
        {
            textBox1.Text = "";
            textBox2.Text = "";
            label1.Text = "";
                
        }

        private void btnProcess_Click(object sender, EventArgs e)
        {
            try
            {
                decimal dInt = 0.0m;
                int dBase = 0;
                string integer = textBox1.Text;
                string bInteger = textBox2.Text;
                string result = string.Empty;
                dInt = System.Convert.ToInt32(integer);
                dBase = System.Convert.ToInt32(bInteger);
                this.Convert(dBase);
                if (dInt <= 0 || dBase < 0)
                    label1.Text = "Integer cannot be 0 or less than 0.";
                if (2 <= dBase || dBase <= 16)
                    label1.Text = "A base between 2 to 16 only.";
            }

            catch (DivideByZeroException)
            {
                label1.Text = "You can not divide by zero.";
            }
            catch (FormatException)
            {
                label1.Text = "No deciamls allowed.";
                if (textBox1.Text == "" || textBox2.Text == "")
                    label1.Text = "Please input a number for both textboxes.";
            }
        }

        private void btnExit_Click(object sender, EventArgs e)
        {
            this.Close();
        }

        private void btnBinary_Click(object sender, EventArgs e)
        {
            try
            {
                decimal dInt = 0.0m;
                string integer = textBox1.Text;

                dInt = System.Convert.ToInt32(integer);
                int remainder;
                string result = string.Empty;
                if (dInt <= 0)
                    label1.Text = "Integer cannot be 0 or less than 0.";
                while (dInt > 1)
                {
                    remainder = (int)(dInt % 2);
                    dInt /= 2;
                    result = remainder.ToString() + result;
                    
                }
                label1.Text = result;
           
            }
            catch (DivideByZeroException)
            {
                label1.Text = "You can not divide by zero.";
            }
            catch (FormatException)
            {
                label1.Text = "No deciamls allowed";
                if (textBox1.Text == "")
                    label1.Text = "Please input a number in both textboxes.";
            }
        }

        private void btnHex_Click(object sender, EventArgs e)
        {
            try
            {
                decimal dInt = 0.0m;
                string integer = textBox1.Text;
                string result = string.Empty;

                dInt = System.Convert.ToInt32(integer);
                int remainder;
                if (dInt <= 0)
                    label1.Text = "Integer cannot be 0 or less than 0.";
                while (dInt > 15)
                {
                    remainder = (int)(dInt % 2);
                    dInt /= 16;
                    result = remainder.ToString() + result;
                }
                label1.Text = result;
                
                    
            }
            catch (DivideByZeroException)
            {
                label1.Text = "You can not divide by zero.";
            }
            catch (FormatException)
            {
                label1.Text = "No deciamls allowed.";
                if (textBox1.Text == "")
                    label1.Text = "Please input a number in both textboxes.";
            }
        }


        private void btnOctal_Click(object sender, EventArgs e)
        {
            try
            {
                decimal dInt = 0.0m;
                string integer = textBox1.Text;
                string result = string.Empty;

                dInt = System.Convert.ToInt32(integer);
                int remainder;
                if (dInt <= 0)
                    label1.Text = "Integer cannot be 0 or less than 0.";
                while (dInt > 7)
                {
                    remainder = (int)(dInt % 2);
                    dInt /= 8;
                    result = remainder.ToString() + result;
                }
                label1.Text = result;

            }
            catch (DivideByZeroException)
            {
                label1.Text = "You can not divide by zero.";
            }
            catch (FormatException)
            {
                label1.Text = "No deciamls allowed.";
                if (textBox1.Text == "")
                    label1.Text = "Please input a number in both textboxes.";
            }
        }


        private void btnBase6_Click(object sender, EventArgs e)
        {
            try
            {
                decimal dInt = 0.0m;
                string integer = textBox1.Text;
                string result = string.Empty;

                dInt = System.Convert.ToInt32(integer);
                int remainder;
                if (dInt <= 0)
                    label1.Text = "Integer cannot be 0 or less than 0.";
                while (dInt > 5)
                {
                    remainder = (int)(dInt % 2);
                    dInt /= 6;
                    result = remainder.ToString() + result;
                }
                label1.Text = result;
                
            }
            catch (DivideByZeroException)
            {
                label1.Text = "You can not divide by zero.";
            }
            catch (FormatException)
            {
                label1.Text = "No deciamls allowed.";
                if (textBox1.Text == "")
                    label1.Text = "Please input a number in both textboxes.";
            }
        }

        private void btnBase9_Click(object sender, EventArgs e)

        {
            try
            {
                decimal dInt = 0.0m;
                string integer = textBox1.Text;
                string result = string.Empty;

                dInt = System.Convert.ToInt32(integer);
                int remainder;
                if (dInt <= 0)
                    label1.Text = "Integer cannot be 0 or less than 0.";
                while (dInt > 8)
                {
                    remainder = (int)(dInt % 2);
                    dInt /= 9;
                    result = remainder.ToString() + result;
                }
                label1.Text = result;
                
            }
            catch (DivideByZeroException)
            {
                label1.Text = "You can not divide by zero.";
            }
            catch (FormatException)
            {
                label1.Text = "No deciamls allowed.";
                if (textBox1.Text == "")
                    label1.Text = "Please input a number in both textboxes.";
            }
        }

    }
}
