# jubjangprapapon
jubjangprapapon
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace WindowsFormsApplication11
{
    public partial class Form1 : Form // ประกาศ ฟรอม 1 เป็นสาธารณะ
    {

        double a;//ประกาศตัวแปลเป็น ดับเบิ้ล
        double b;
        double c;
        double d;
        double e;
        Form2 f2;//ประกาศฟร์ม2   เท่ากับ f2
        public Form1() 
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            try
            {
                f2 = new Form2(); //ประกาศ f2 ให้เปิดฟร์ม2 
                f2.label21.Text = comboBox4.Text; //ให้ข้อมูลในcomboBox4 ไปโชว์ในฟอร์ม 2 ของ label21
                f2.label2.Text = textBox1.Text; //ให้ข้อมูลในtextBox1 ไปโชว์ในฟอร์ม 2 ของ label2
                f2.label4.Text = textBox3.Text; //ให้ข้อมูลในtextBox3 ไปโชว์ในฟอร์ม 2 ของ label4
                f2.label6.Text = textBox2.Text; //ให้ข้อมูลในtextBox2 ไปโชว์ในฟอร์ม 2 ของ label6
                f2.label10.Text = comboBox3.Text; //ให้ข้อมูลในcomboBox3 ไปโชว์ในฟอร์ม 2 ของ label10
                f2.label27.Text = textBox4.Text; //ให้ข้อมูลในtextBox4 ไปโชว์ในฟอร์ม 2 ของ label27
                f2.label8.Text = comboBox1.Text; //ให้ข้อมูลในcomboBox1 ไปโชว์ในฟอร์ม 2 ของ label8
                f2.Show(); // เป็นคำสั่งเปิดฟร์ม 2
                if (radioButton1.Checked == true) //ถ้าเรากดปุ่มradioButton1นี้เป็นจริง
                {
                    f2.label26.Text = radioButton1.Text;//ให้ข้อมูลใน radioButton1 ไปโชว์ใน label26 ใน ฟอร์ม ที่ 2
                }
                else if (radioButton2.Checked == true) //ถ้าเรากดปุ่มradioButton2 นี้เป็นจริง
                {
                    f2.label26.Text = radioButton2.Text; //ให้ข้อมูลใน radioButton2 ไปโชว์ใน label26 ใน ฟอร์ม ที่ 2
                }
                if (radioButton3.Checked == true) //ถ้าเรากดปุ่มradioButton3 นี้เป็นจริง
                {
                    f2.label25.Text = radioButton3.Text;//ให้ข้อมูลใน radioButton3 ไปโชว์ใน label25 ใน ฟอร์ม ที่ 2
                }
                else if (radioButton4.Checked == true) //ถ้าเรากดปุ่มradioButton4 นี้เป็นจริง
                {
                    f2.label25.Text = radioButton4.Text;//ให้ข้อมูลใน radioButton4 ไปโชว์ใน label25 ใน ฟอร์ม ที่ 2
                }
                else if (radioButton5.Checked == true)//ถ้าเรากดปุ่มradioButton5 นี้เป็นจริง
                {
                    f2.label25.Text = radioButton5.Text;//ให้ข้อมูลใน radioButton5 ไปโชว์ใน label25 ใน ฟอร์ม ที่ 2
                }
                else if (radioButton6.Checked == true)//ถ้าเรากดปุ่มradioButton6 นี้เป็นจริง
                {
                    f2.label25.Text = radioButton6.Text;//ให้ข้อมูลใน radioButton6 ไปโชว์ใน label25 ใน ฟอร์ม ที่ 2
                }
                else if (radioButton7.Checked == true)//ถ้าเรากดปุ่มradioButton7 นี้เป็นจริง
                {
                    f2.label25.Text = radioButton7.Text;//ให้ข้อมูลใน radioButton7 ไปโชว์ใน label25 ใน ฟอร์ม ที่ 2
                }
                else if (radioButton8.Checked == true)//ถ้าเรากดปุ่มradioButton8 นี้เป็นจริง
                {
                    f2.label25.Text = radioButton8.Text;//ให้ข้อมูลใน radioButton8 ไปโชว์ใน label25 ใน ฟอร์ม ที่ 2
                }

               
                double p = double.Parse(textBox4.Text); //แปลงข้อมูลจากtextBox4เป็น  double ในตัวแปล p
                vu(p);//ตัวแปล p คูณกับ Vu
            }
            catch // ดักerror ในกรณีที่ไม่เข้ากรณีที่กล่าวมาข้างต้น
            {
                MessageBox.Show("กรุณาใส่ข้อมูลให้ถูกต้อง", "ตรวจสอบ", MessageBoxButtons.OK, MessageBoxIcon.Warning); //ให้ขั้น MessageBox ว่ากรุณาใส่ข้อมูลให้ถูกต้อง
            }

        }

            public void vu(double e) //สร้าง Method ขั้นมาเก็บราคา เครื่องบิน
        {
            try
            {


                if (radioButton9.Checked == true)//ถ้าเรากดปุ่มradioButton9 นี้เป็นจริง
                {
                    if (radioButton1.Checked)//ถ้าเรากดปุ่มradioButton1 คือปุ่ม มี
                    {
                        double variabletex4 = double.Parse(textBox4.Text);//แปลงข้อมูลจาก textBox4 เป็น double
                        e = variabletex4 * 350; //เอาจำนวณที่นั่งไปคูณกับ ค่าประกันเครื่อง แล้วเก็บไว้ในตัวแปล e คือราคา 
                        a = (1200 * variabletex4); //เอาจำนวณ Class ไปคูณกับ ที่นั่ง แล้วเก็บไว้ในตัวแปล a คือ Classที่นั่ง ประหยัด
                        double z = e + a; // เอาตัวแปล e + a แล้วเก็บไว้ในตัวแปล z
                        f2.label15.Text = z.ToString() + "   บาท"; //แปลงตัวแปล z เป็นข้อความแล้วโชว์ใน label15 ในฟอร์ม 2
                        f2.label28.Text = "ประหยัด"; //ให้ label28 โชว์ข้อความว่าประหยัดใน ฟอร์ม 2
                    }
                    if (radioButton2.Checked)//ถ้าเรากดปุ่มradioButton2 คือปุ่ม ไม่มี

                    {
                        a = 1200 * e; //1200*ราคา
                        f2.label15.Text = a.ToString() + "   บาท"; //แปลงตัวแปล z เป็นข้อความแล้วโชว์ใน label15 ในฟอร์ม 2
                        f2.label28.Text = "ประหยัด";//ให้ label28 โชว์ข้อความว่าประหยัดใน ฟอร์ม 2
                    }
                }

                if (radioButton10.Checked == true)//ถ้าเรากดปุ่มradioButton10 นี้เป็นจริง
                {
                    if (radioButton1.Checked) //ถ้าเรากดปุ่มradioButton1 คือปุ่ม มี

                    {
                        double A = double.Parse(textBox4.Text); //แปลงข้อมูลจาก textBox4 เป็น double
                        e = A * 350; //เอาจำนวณที่นั่งไปคูณกับ ค่าประกันเครื่อง แล้วเก็บไว้ในตัวแปล e คือราคา 
                        a = (3500 * A); //เอาจำนวณ Class ไปคูณกับ ที่นั่ง แล้วเก็บไว้ในตัวแปล a คือ Classที่นั่ง ปกติ
                        double z = e + a;// เอาตัวแปล e + a แล้วเก็บไว้ในตัวแปล z
                        f2.label15.Text = z.ToString() + "   บาท"; //แปลงตัวแปล z เป็นข้อความแล้วโชว์ใน label15 ในฟอร์ม 2
                        f2.label28.Text = "ปกติ";//ให้ label28 โชว์ข้อความว่าปกติใน ฟอร์ม 2
                    }
                    if (radioButton2.Checked)//ถ้าเรากดปุ่มradioButton2 คือปุ่ม ไม่มี

                    {
                        a = (3500 * e); //3500*ราคา
                        f2.label15.Text = a.ToString() + "   บาท";//แปลงตัวแปล z เป็นข้อความแล้วโชว์ใน label15 ในฟอร์ม 2
                        f2.label28.Text = "ปกติ";//ให้ label28 โชว์ข้อความว่าปกติใน ฟอร์ม 2
                    }

                }

                if (radioButton11.Checked == true)//ถ้าเรากดปุ่มradioButton11 นี้เป็นจริง
                {
                    {
                        if (radioButton1.Checked)//ถ้าเรากดปุ่มradioButton1 คือปุ่ม มี

                        {
                            double A = double.Parse(textBox4.Text);//แปลงข้อมูลจาก textBox4 เป็น double
                            e = A * 350;//เอาจำนวณที่นั่งไปคูณกับ ค่าประกันเครื่อง แล้วเก็บไว้ในตัวแปล e คือราคา
                            a = (5800 * A);//เอาจำนวณ Class ไปคูณกับ ที่นั่ง แล้วเก็บไว้ในตัวแปล a คือ Classที่นั่ง พิเศษ
                            double z = e + a;// เอาตัวแปล e + a แล้วเก็บไว้ในตัวแปล z
                            f2.label15.Text = z.ToString() + "   บาท";//แปลงตัวแปล z เป็นข้อความแล้วโชว์ใน label15 ในฟอร์ม 2
                            f2.label28.Text = "พิเศษ";//ให้ label28 โชว์ข้อความว่าพิเศษใน ฟอร์ม 2
                        }
                        if (radioButton2.Checked)//ถ้าเรากดปุ่มradioButton2 คือปุ่ม ไม่มี

                        {
                            a = (5800 * e);//5800*ราคา
                            f2.label15.Text = a.ToString() + "   บาท";//แปลงตัวแปล a เป็นข้อความแล้วโชว์ใน label15 ในฟอร์ม 2
                            f2.label28.Text = "พิเศษ";//ให้ label28 โชว์ข้อความว่าพิเศษใน ฟอร์ม 2
                        }

                    }
                }
            }

            catch
            {

            }
        }

        private void button2_Click(object sender, EventArgs e)
        {
            Close();//ปุมกดออก

        }

        private void textBox1_KeyPress(object sender, KeyPressEventArgs e)
        {
           
        }

        private void textBox2_TextChanged(object sender, EventArgs e)
        {

        }

        private void textBox2_KeyPress(object sender, KeyPressEventArgs e)
        {
        }

        private void textBox3_KeyPress(object sender, KeyPressEventArgs e)
        {
            
        }

        private void textBox4_KeyPress(object sender, KeyPressEventArgs e)
        {
           
        }

        private void textBox1_TextChanged(object sender, EventArgs e)
        {

        }
        private string calulateAge(string dateDOB)     
            {
            int now = int.Parse(DateTime.Today.ToString("yyyyMMdd"));//ตั้งตัวแปลของวัน เดือน ปี 
            int dob = int.Parse(dateDOB);//กำหนดตัวแปล ปี พศ.ที่เกิด
            string dif = (now - dob).ToString();//เอาปีปัจจุบันลบกับปีที่เกิด
            string age = "0"; //กำหนดอายุไว้เปน 0 
            if (dif.Length > 4)
                age = dif.Substring(0, dif.Length - 4);
            return age;
        }
        private void dateTimePicker1_ValueChanged(object sender, EventArgs e)
        {
            textBox3.Text = calulateAge(dateTimePicker1.Value.ToString("yyyyMMdd"));//ให้อายุที่คำวาณมาไปโชว์ใน textBox3
        }

        public void comboBox1_SelectedIndexChanged(object sender, EventArgs e)
        {
            if (comboBox1.SelectedItem == "การบินไทย") //ถ้าเรากดเลือก สายการบินไทยในcomboBox1 จะแสดงรายละเอียดว่า จากใหนถึงไหนในcomboBox3 และเวลาใน radioButton3
            {
                comboBox3.Items.Clear(); //ลบข้อมูลออกเมื่อเราเปลี่ยนสายการบิน
                comboBox3.Items.Add("กรุงเทพ(BKK) - กระบี่(KBV)");//เมื่อกดเลือก การบินไทยจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพ(BKK) - เกาะสมุย(USM)");//เมื่อกดเลือก การบินไทยจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพ(BKK) - ขอนแก่น(KKC)");//เมื่อกดเลือก การบินไทยจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพ(BKK) - เชียงราย(CEI)");//เมื่อกดเลือก การบินไทยจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("ขอนแก่น(KKC) - กรุงเทพ(BKK)");//เมื่อกดเลือก การบินไทยจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("อุดรธานี(UTH) - กรุงเทพ(BKK)");//เมื่อกดเลือก การบินไทยจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพ(BKK) - อุดรธานี(UTH)");//เมื่อกดเลือก การบินไทยจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("อุบลราชธานี(UBP) - กรุงเทพ(BKK)");//เมื่อกดเลือก การบินไทยจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เชียงราย(CEI) - กรุงเทพ(BKK)");//เมื่อกดเลือก การบินไทยจะแสดงข้อความใน comboBox3 
                radioButton3.Text = "08:00 - 09:20";//เมื่อกดเลือก การบินไทยจะแสดงเวลาใน  radioButton3
                radioButton4.Text = "12:05 - 13:25";//เมื่อกดเลือก การบินไทยจะแสดงเวลาใน radioButton4
                radioButton5.Text = "15:30 - 15:00";//เมื่อกดเลือก การบินไทยจะแสดงเวลาใน  radioButton5
                radioButton6.Text = "14:45 - 15:40";//เมื่อกดเลือก การบินไทยจะแสดงเวลาใน  radioButton6
                radioButton7.Text = "16:20 - 17:15";//เมื่อกดเลือก การบินไทยจะแสดงเวลาใน  radioButton7
                radioButton8.Text = "20:00 - 21:00";//เมื่อกดเลือก การบินไทยจะแสดงเวลาใน  radioButton8
            }
            if (comboBox1.SelectedItem == "นกแอร์") //ถ้าเรากดเลือก สายการบินนกแอร์ในcomboBox1 จะแสดงรายละเอียดว่า จากใหนถึงไหนในcomboBox3 และเวลาใน radioButton3
            {
                comboBox3.Items.Clear(); //ลบข้อมูลออกเมื่อเราเปลี่ยนสายการบิน
                comboBox3.Items.Add("กรุงเทพฯดอนเมือง(DMK) - เชียงใหม่(CNX)");//เมื่อกดเลือก การบินนกแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพฯดอนเมือง(DMK) - เชียงราย(CEI)");//เมื่อกดเลือก การบินนกแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("พิษณุโลก(PHS) - กรุงเทพฯดอนเมือง(DMK)");//เมื่อกดเลือก การบินนกแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพฯดอนเมือง(DMK) - ขอนแก่น(KKC)");//เมื่อกดเลือก การบินนกแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("สกลนคร(SNO) - กรุงเทพฯดอนเมือง(DMK)");//เมื่อกดเลือก การบินนกแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพฯดอนเมือง(DMK) - เลย(LOE)");//เมื่อกดเลือก การบินนกแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เชียงใหม่(CNX) - อุดรธานี(UTH)");//เมื่อกดเลือก การบินนกแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("ลำปาง(LPT) - กรุงเทพฯดอนเมือง(DMK)");//เมื่อกดเลือก การบินนกแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("ตรัง(TST) - กรุงเทพฯดอนเมือง(DMK)");//เมื่อกดเลือก การบินนกแอร์จะแสดงข้อความใน comboBox3 
                radioButton3.Text = "06:05 - 07:15";//เมื่อกดเลือก การบินนกแอร์จะแสดงเวลาใน  radioButton3
                radioButton4.Text = "06:50 - 08:00";//เมื่อกดเลือก การบินนกแอร์จะแสดงเวลาใน  radioButton4
                radioButton5.Text = "09:05 - 10:15";//เมื่อกดเลือก การบินนกแอร์จะแสดงเวลาใน  radioButton5
                radioButton6.Text = "12:40 - 13:50";//เมื่อกดเลือก การบินนกแอร์จะแสดงเวลาใน  radioButton6
                radioButton7.Text = "14:20 - 15:30";//เมื่อกดเลือก การบินนกแอร์จะแสดงเวลาใน  radioButton7
                radioButton8.Text = "17:00 - 18:05";//เมื่อกดเลือก การบินนกแอร์จะแสดงเวลาใน  radioButton8
            }
            if (comboBox1.SelectedItem == "ไทยแอร์เอเชีย") //ถ้าเรากดเลือก สายการบินไทยแอร์เอเชียในcomboBox1 จะแสดงรายละเอียดว่า จากใหนถึงไหนในcomboBox3 และเวลาใน radioButton3
            {
                comboBox3.Items.Clear();//ลบข้อมูลออกเมื่อเราเปลี่ยนสายการบิน
                comboBox3.Items.Add("ภูเก็ต(HKT) - กรุงเทพฯดอนเมือง(DMK)");//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("หาดใหญ่(HDY) - กรุงเทพฯดอนเมือง(DMK)");//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพฯดอนเมือง(DMK) - เชียงราย(CEI)");//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("พิษณุโลก(PHS) - กรุงเทพฯดอนเมือง(DMK)");//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพฯดอนเมือง(DMK) - ขอนแก่น(KKC)");//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("ขอนแก่น(KKC) - กรุงเทพฯดอนเมือง(DMK)");//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพฯดอนเมือง(DMK) - อุดรธานี(UTH)");//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("อุดรธานี(UTH) - กรุงเทพฯ ดอนเมือง(DMK)");//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("ขอนแก่น(KKC) - เชียงใหม่(CNX)");//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงข้อความใน comboBox3 
                radioButton3.Text = "09:15 - 11:20";//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงเวลาใน  radioButton3
                radioButton4.Text = "07:00 - 08:10";//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงเวลาใน  radioButton4
                radioButton5.Text = "13:10 - 15:15";//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงเวลาใน  radioButton5
                radioButton6.Text = "12:40 - 13:50";//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงเวลาใน  radioButton6
                radioButton7.Text = "14:20 - 15:35";//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงเวลาใน  radioButton7
                radioButton8.Text = "20:15 - 22:15";//เมื่อกดเลือก การบินไทยแอร์เอเชียจะแสดงเวลาใน  radioButton8
            }
            if (comboBox1.SelectedItem == "บางกอกแอร์เวย์")//ถ้าเรากดเลือก สายการบินบางกอกแอร์เวย์ในcomboBox1 จะแสดงรายละเอียดว่า จากใหนถึงไหนในcomboBox3 และเวลาใน radioButton3
            {
                comboBox3.Items.Clear();//ลบข้อมูลออกเมื่อเราเปลี่ยนสายการบิน
                comboBox3.Items.Add("กรุงเทพฯสุวรรณภูมิ(BKK) - เชียงใหม่(CNX)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เชียงใหม่(CNX) - กรุงเทพฯสุวรรณภูมิ(BKK)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพฯสุวรรณภูมิ(BKK) - ภูเก็ต(HKT)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("ภูเก็ต(HKT) - กรุงเทพฯสุวรรณภูมิ(BKK)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เกาะสมุย(USM) - กรุงเทพฯสุวรรณภูมิ(BKK)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพฯสุวรรณภูมิ (BKK) - ลำปาง(LPT)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("ลำปาง(LPT) - กรุงเทพฯสุวรรณภูมิ(BKK)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพฯสุวรรณภูมิ(BKK) - เชียงราย(CEI)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เชียงราย(CEI) - กรุงเทพฯสุวรรณภูมิ(BKK)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพฯสุวรรณภูมิ(BKK) - สุโขทัย(THS)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("สุโขทัย(THS) - กรุงเทพฯสุวรรณภูมิ(BKK)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เชียงใหม่(CNX) - กระบี่(KBV)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กระบี่(KBV) - สมุย(USM)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("ภูเก็ต(HKT) - หาดใหญ่(HDY)");//เมื่อกดเลือก การบินบางกอกแอร์เวย์จะแสดงข้อความใน comboBox3 
                radioButton3.Text = "06:55 - 07:05";//เมื่อกดเลือก สายการบินบางกอกแอร์เวย์จะแสดงเวลาใน  radioButton3
                radioButton4.Text = "07:00 - 08:15";//เมื่อกดเลือก สายการบินบางกอกแอร์เวย์จะแสดงเวลาใน  radioButton4
                radioButton5.Text = "09:55 - 11:00";//เมื่อกดเลือก สายการบินบางกอกแอร์เวย์จะแสดงเวลาใน  radioButton5
                radioButton6.Text = "11:45 - 12:50";//เมื่อกดเลือก สายการบินบางกอกแอร์เวย์จะแสดงเวลาใน  radioButton6
                radioButton7.Text = "12:30 - 13:45";//เมื่อกดเลือก สายการบินบางกอกแอร์เวย์จะแสดงเวลาใน  radioButton7
                radioButton8.Text = "20:15 - 17:10";//เมื่อกดเลือก สายการบินบางกอกแอร์เวย์จะแสดงเวลาใน  radioButton8
            }
            if (comboBox1.SelectedItem == "กานต์แอร์")//ถ้าเรากดเลือก สายการบินกานต์แอร์ในcomboBox1 จะแสดงรายละเอียดว่า จากใหนถึงไหนในcomboBox3 และเวลาใน radioButton3
            {
                comboBox3.Items.Clear();//ลบข้อมูลออกเมื่อเราเปลี่ยนสายการบิน
                comboBox3.Items.Add("เที่ยวบินตรง เชียงใหม่ - แม่ฮ่องสอน");//เมื่อกดเลือก การบินกานต์แอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เที่ยวบินตรง เชียงใหม่ - ปาย");//เมื่อกดเลือก การบินกานต์แอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เที่ยวบินตรง เชียงใหม่ - น่าน");//เมื่อกดเลือก การบินกานต์แอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เที่ยวบินตรง เชียงใหม่ - พิษณุโลก");//เมื่อกดเลือก การบินกานต์แอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เที่ยวบินตรง เชียงใหม่ - เชียงราย");//เมื่อกดเลือก การบินกานต์แอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เที่ยวบินตรง เชียงใหม่ - ขอนแก่น");//เมื่อกดเลือก การบินกานต์แอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เที่ยวบินตรง เชียงใหม่ - อุบลฯ");//เมื่อกดเลือก การบินกานต์แอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เที่ยวบินตรง เชียงใหม่ - หัวหิน");//เมื่อกดเลือก การบินกานต์แอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เที่ยวบินตรง เชียงใหม่ - อู่ตะเภา");//เมื่อกดเลือก การบินกานต์แอร์จะแสดงข้อความใน comboBox3 
                radioButton3.Text = "07:00 - 08:25";//เมื่อกดเลือก สายการบินบางกานต์แอร์จะแสดงเวลาใน  radioButton3
                radioButton4.Text = "10:20 - 11:45";//เมื่อกดเลือก สายการบินบางกานต์แอร์จะแสดงเวลาใน  radioButton4
                radioButton5.Text = "12:15 - 13:40";//เมื่อกดเลือก สายการบินบางกานต์แอร์จะแสดงเวลาใน  radioButton5
                radioButton6.Text = "16:10 - 17:35";//เมื่อกดเลือก สายการบินบางกานต์แอร์จะแสดงเวลาใน  radioButton6
                radioButton7.Text = "19:05 - 20:30";//เมื่อกดเลือก สายการบินบางกานต์แอร์จะแสดงเวลาใน  radioButton7
                radioButton8.Text = "21:55 - 23:20";//เมื่อกดเลือก สายการบินบางกานต์แอร์จะแสดงเวลาใน  radioButton8
            }
            if (comboBox1.SelectedItem == "การบินไทยสมายล์")//ถ้าเรากดเลือก สายการบินไทยสมายล์ในcomboBox1 จะแสดงรายละเอียดว่า จากใหนถึงไหนในcomboBox3 และเวลาใน radioButton3
            {
                comboBox3.Items.Clear();//ลบข้อมูลออกเมื่อเราเปลี่ยนสายการบิน
                comboBox3.Items.Add("กรุงเทพฯ(สุวรรณภูมิ) -	สุราษฎร์ธานี");//เมื่อกดเลือก การบินไทยสมายล์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("เชียงราย - กรุงเทพฯ(สุวรรณภูมิ");//เมื่อกดเลือก การบินไทยสมายล์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("ขอนแก่น	- กรุงเทพฯ(ดอนเมือง)");//เมื่อกดเลือก การบินไทยสมายล์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("ขอนแก่น - กรุงเทพฯ(สุวรรณภูมิ)");//เมื่อกดเลือก การบินไทยสมายล์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("อุบลราชธานี - กรุงเทพฯ(สุวรรณภูมิ)");//เมื่อกดเลือก การบินไทยสมายล์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("อุดรธานี - 	กรุงเทพฯ(สุวรรณภูมิ)");//เมื่อกดเลือก การบินไทยสมายล์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพฯ(สุวรรณภูมิ) - อุดรธานี");//เมื่อกดเลือก การบินไทยสมายล์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กระบี่ - กรุงเทพฯ(สุวรรณภูมิ)");//เมื่อกดเลือก การบินไทยสมายล์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("ภูเก็ต - กรุงเทพฯ(ดอนเมือง)");//เมื่อกดเลือก การบินไทยสมายล์จะแสดงข้อความใน comboBox3 
                radioButton3.Text = "08:30 - 09:45";//เมื่อกดเลือก สายการบินการบินไทยสมายล์จะแสดงเวลาใน  radioButton3
                radioButton4.Text = "10:15 - 11:25";//เมื่อกดเลือก สายการบินการบินไทยสมายล์จะแสดงเวลาใน  radioButton4
                radioButton5.Text = "12:15 - 13:40";//เมื่อกดเลือก สายการบินการบินไทยสมายล์จะแสดงเวลาใน  radioButton5
                radioButton6.Text = "18:30 - 19:55";//เมื่อกดเลือก สายการบินการบินไทยสมายล์จะแสดงเวลาใน  radioButton6
                radioButton7.Text = "20:35 - 22:00";//เมื่อกดเลือก สายการบินการบินไทยสมายล์จะแสดงเวลาใน  radioButton7
                radioButton8.Text = "22:10 - 00:10";//เมื่อกดเลือก สายการบินการบินไทยสมายล์จะแสดงเวลาใน  radioButton8
            }
            if (comboBox1.SelectedItem == "ไลอ้อนแอร์")//ถ้าเรากดเลือก สายการบินไลอ้อนแอร์ในcomboBox1 จะแสดงรายละเอียดว่า จากใหนถึงไหนในcomboBox3 และเวลาใน radioButton3
            {
                comboBox3.Items.Clear();//ลบข้อมูลออกเมื่อเราเปลี่ยนสายการบิน
                comboBox3.Items.Add("กรุงเทพฯดอนเมือง(DMK) - เชียงใหม่(CNX)");//เมื่อกดเลือก การบินไลอ้อนแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("นครศรีธรรมราช(NST) - กรุงเทพฯดอนเมือง(DMK)");//เมื่อกดเลือก การบินไลอ้อนแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพฯดอนเมือง(DMK) - อุดรธานี(UTH)");//เมื่อกดเลือก การบินไลอ้อนแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("อุดรธานี(UTH) - กรุงเทพฯดอนเมือง(DMK)");//เมื่อกดเลือก การบินไลอ้อนแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("อุดรธานี(UTH) - หาดใหญ่(HDY)");//เมื่อกดเลือก การบินไลอ้อนแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("หาดใหญ่(HDY) - อุดรธานี(UTH)");//เมื่อกดเลือก การบินไลอ้อนแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กรุงเทพฯดอนเมือง(DMK) - อุบลราชธานี(UBP)");//เมื่อกดเลือก การบินไลอ้อนแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("ภูเก็ต(HKT) - กรุงเทพฯ ดอนเมือง(DMK)");//เมื่อกดเลือก การบินไลอ้อนแอร์จะแสดงข้อความใน comboBox3 
                comboBox3.Items.Add("กระบี(KBV) - กรุงเทพฯดอนเมือง(DMK)");//เมื่อกดเลือก การบินไลอ้อนแอร์จะแสดงข้อความใน comboBox3 
                radioButton3.Text = "08:40 - 10:10";//เมื่อกดเลือก สายการบินไลอ้อนแอร์จะแสดงเวลาใน  radioButton3
                radioButton4.Text = "11:15 - 12:35";//เมื่อกดเลือก สายการบินไลอ้อนแอร์จะแสดงเวลาใน  radioButton3
                radioButton5.Text = "15:20 - 16:30";//เมื่อกดเลือก สายการบินไลอ้อนแอร์จะแสดงเวลาใน  radioButton3
                radioButton6.Text = "18:00 - 19:20";//เมื่อกดเลือก สายการบินไลอ้อนแอร์จะแสดงเวลาใน  radioButton3
                radioButton7.Text = "20:35 - 22:00";//เมื่อกดเลือก สายการบินไลอ้อนแอร์จะแสดงเวลาใน  radioButton3
                radioButton8.Text = "22:10 - 00:00";//เมื่อกดเลือก สายการบินไลอ้อนแอร์จะแสดงเวลาใน  radioButton3
            }

        }

        private void textBox3_TextChanged(object sender, EventArgs e)
        {
            
        }
    }
}
