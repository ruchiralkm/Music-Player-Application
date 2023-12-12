using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
using System.IO;
using System.Diagnostics;
using static System.Windows.Forms.VisualStyles.VisualStyleElement;

namespace Music_Player
{
    public partial class form1 : Form
    {
        public form1()
        {
            InitializeComponent();
        }
        string[] paths, files;

        private void bunifuPictureBox1_Click(object sender, EventArgs e)
        {

        }

        private void btnPlaying_Click(object sender, EventArgs e)
        {
            Indicator.Top = btnPlaying.Top + 15;
            bunifuPages1.SetPage(0);
        }

        private void btnExplore_Click(object sender, EventArgs e)
        {
            Indicator.Top = btnPlaying.Top + 95;
            bunifuPages1.SetPage(1);
        }

        private void bunifuImageButton1_Click(object sender, EventArgs e)
        {
            Environment.Exit(0);
        }

        private void label3_Click(object sender, EventArgs e)
        {

        }

        private void tabPage1_Click(object sender, EventArgs e)
        {

        }

        private void track_list_SelectedIndexChanged(object sender, EventArgs e)
        {
            player.URL = paths[track_list.SelectedIndex];
            player.Ctlcontrols.play();
            try
            {
                var file = TagLib.File.Create(paths[track_list.SelectedIndex]);
                var bin = (byte[])(file.Tag.Pictures[0].Data.Data);
                pictureBox4.Image = Image.FromStream(new MemoryStream(bin));
            }
            catch 
            {

            }
        }

        private void bunifuImageButton3_Click(object sender, EventArgs e)
        {
            player.Ctlcontrols.stop();
            bunifuHSlider1.Value = 0;
        }

        private void bunifuImageButton5_Click(object sender, EventArgs e)
        {
            if(track_list.SelectedIndex<track_list.Items.Count-1)
            {
                track_list.SelectedIndex = track_list.SelectedIndex + 1;
            }
        }

        private void bunifuImageButton4_Click(object sender, EventArgs e)
        {
            if(track_list.SelectedIndex>0)
            {
                track_list.SelectedIndex = track_list.SelectedIndex - 1;
            }
        }

        private void timer1_Tick(object sender, EventArgs e)
        {
            if(player.playState==WMPLib.WMPPlayState.wmppsPlaying)
            {
                bunifuHSlider1.Maximum = (int)player.Ctlcontrols.currentItem.duration;
                bunifuHSlider1.Value = (int)player.Ctlcontrols.currentPosition;
            }
            try
            {
                label10.Text = player.Ctlcontrols.currentPositionString;
            }
            catch
            {

            }
        }

        private void bunifuHSlider2_Scroll(object sender, Utilities.BunifuSlider.BunifuHScrollBar.ScrollEventArgs e)
        {
            player.settings.volume = bunifuHSlider2.Value;
        }

        private void bunifuHSlider1_MouseDown(object sender, MouseEventArgs e)
        {
            player.Ctlcontrols.currentPosition = player.currentMedia.duration * e.X / bunifuHSlider1.Width;
        }

        private void bunifuImageButton2_Click(object sender, EventArgs e)
        {
            if(player.status.ToLower().Contains("playing"))
            {
                player.Ctlcontrols.pause();
            }
            else
            {
                player.Ctlcontrols.play();
            }
        }

        private void player_PlayStateChangee(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
        {
            label3.Text = player.status;
            label11.Text = player.status;
            label12.Text = player.status;
            label13.Text = player.status;

            imagevisualizer.Visible = player.status.ToLower().Contains("playing");
            label4.Visible = player.status.ToLower().Contains("playing");
            label5.Visible = player.status.ToLower().Contains("playing");
            label11.Visible = player.status.ToLower().Contains("playing");
            label7.Visible = player.status.ToLower().Contains("playing");
            label6.Visible = player.status.ToLower().Contains("playing");
            label12.Visible = player.status.ToLower().Contains("playing");
            label9.Visible = player.status.ToLower().Contains("playing");
            label8.Visible = player.status.ToLower().Contains("playing");
            label13.Visible = player.status.ToLower().Contains("playing");
            label15.Visible = player.status.ToLower().Contains("paused");
        }

        private void tabPage2_Click(object sender, EventArgs e)
        {

        }

        private void bunifuButton4_Click(object sender, EventArgs e)
        {
            Indicator.Top = btnPlaying.Top + 170;
            bunifuPages1.SetPage(2);
        }

        private void bunifuButton5_Click(object sender, EventArgs e)
        {
            Indicator.Top = btnPlaying.Top - 260;
            bunifuPages1.SetPage(4);
        }

        private void panel1_Paint(object sender, PaintEventArgs e)
        {

        }

        private void label14_Click(object sender, EventArgs e)
        {

        }

        private void bunifuImageButton7_Click(object sender, EventArgs e)
        {
            panel1.BackColor = Color.FromArgb(36, 36, 36);
            panel3.BackColor = Color.FromArgb(52, 52, 52);
            panel2.BackColor = Color.FromArgb(52, 52, 52);
            label3.ForeColor = Color.WhiteSmoke;
            label1.ForeColor = Color.WhiteSmoke;
            label3.BackColor = Color.FromArgb(52, 52, 52);

            //left buttons
            //Play button
            /*
            btnPlaying.OnIdleState.ForeColor = Color.Black;
            btnPlaying.ForeColor = Color.White;

            btnExplore.OnIdleState.ForeColor = Color.Black;
            btnExplore.ForeColor = Color.White;

            bunifuButton4.OnIdleState.ForeColor = Color.Black;
            bunifuButton4.ForeColor = Color.White;

            bunifuButton3.OnIdleState.ForeColor = Color.Black;
            bunifuButton3.ForeColor = Color.White;

            bunifuButton5.OnIdleState.ForeColor = Color.Black;
            bunifuButton5.ForeColor = Color.White;

            bunifuButton6.OnIdleState.ForeColor = Color.Black;
            bunifuButton6.ForeColor = Color.White;*/

        }

        private void bunifuImageButton6_Click(object sender, EventArgs e)
        {
            panel1.BackColor = Color.Gainsboro;
            panel3.BackColor = Color.ForestGreen;
            panel2.BackColor = Color.WhiteSmoke;
            label3.ForeColor = Color.Black;
            label3.BackColor = Color.WhiteSmoke;
            label1.ForeColor = Color.Black;

            //left nuttons
            //Play button
            /*
            btnPlaying.OnIdleState.ForeColor = Color.Black;
            btnPlaying.ForeColor = Color.Black;
            btnPlaying.OnDisabledState.ForeColor = Color.White;

            btnExplore.OnIdleState.ForeColor = Color.Black;
            btnExplore.ForeColor = Color.Black;
            btnExplore.OnDisabledState.ForeColor = Color.White;

            bunifuButton4.OnIdleState.ForeColor = Color.Black;
            bunifuButton4.ForeColor = Color.Black;
            bunifuButton4.OnDisabledState.ForeColor = Color.White;

            bunifuButton3.OnIdleState.ForeColor = Color.Black;
            bunifuButton3.ForeColor = Color.Black;
            bunifuButton3.OnDisabledState.ForeColor = Color.White;

            bunifuButton5.OnIdleState.ForeColor = Color.Black;
            bunifuButton5.ForeColor = Color.Black;
            bunifuButton5.OnDisabledState.ForeColor = Color.White;

            bunifuButton6.OnIdleState.ForeColor = Color.Black;
            bunifuButton6.ForeColor = Color.Black;
            bunifuButton6.OnDisabledState.ForeColor = Color.White;*/

        }

        private void bunifuImageButton8_Click(object sender, EventArgs e)
        {
            panel1.BackColor = Color.FromArgb(0, 150, 255);
            panel3.BackColor = Color.FromArgb(65, 105, 255);
            panel2.BackColor = Color.FromArgb(65, 105, 255);
            label3.ForeColor = Color.WhiteSmoke;
            label3.BackColor = Color.FromArgb(65, 105, 255);

            //left buttons
            //btnPlaying.ForeColor = Color.Black;

        }

        private void bunifuImageButton9_Click(object sender, EventArgs e)
        {
            panel1.BackColor = Color.FromArgb(255, 234, 0);
            panel3.BackColor = Color.FromArgb(250, 250, 51);
            panel2.BackColor = Color.FromArgb(250, 250, 51);
            label3.ForeColor = Color.Black;
            label3.BackColor = Color.FromArgb(250, 250, 51);
            label1.ForeColor = Color.Black;

            //left buttons
            //btnPlaying.ForeColor = Color.Black;

        }

        private void label11_Click(object sender, EventArgs e)
        {

        }

        private void bunifuButton3_Click(object sender, EventArgs e)
        {
            Indicator.Top = btnPlaying.Top + 260;
            bunifuPages1.SetPage(3);
        }

        private void bunifuButton6_Click(object sender, EventArgs e)
        {
            Indicator.Top = btnPlaying.Top - 260;
            bunifuPages1.SetPage(5);
        }

        private void bunifuButton2_Click(object sender, EventArgs e)
        {
            System.Diagnostics.Process.Start("https://ruchiralk.000webhostapp.com/");
        }

        private void pictureBox7_Click(object sender, EventArgs e)
        {

        }

        private void pictureBox8_Click(object sender, EventArgs e)
        {

        }

        private void pictureBox6_Click(object sender, EventArgs e)
        {

        }

        private void label2_Click(object sender, EventArgs e)
        {

        }

        private void bunifuImageButton10_Click(object sender, EventArgs e)
        {
            System.Diagnostics.Process.Start("https://ruchiralk.000webhostapp.com/mfeedback.html");
        }

        private void bunifuButton1_Click(object sender, EventArgs e)
        {
            
                OpenFileDialog ofd = new OpenFileDialog();
                ofd.Multiselect = true;
            
                if (ofd.ShowDialog() == System.Windows.Forms.DialogResult.OK)
                {
                
                    files = ofd.FileNames;
                    paths = ofd.FileNames;
                    for (int x = 0; x < files.Length; x++)
                    {
                        track_list.Items.Add(files[x]);
                    }
                }
        }   
    }
}
