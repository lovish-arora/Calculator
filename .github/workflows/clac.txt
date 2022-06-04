import java.awt.*;
import java.awt.event.*;
import java.applet.*;
import javax.swing.*;
public class mycalc extends Applet implements ActionListener
{
    double num = 0;
    char op = ' ';
    int i = 0;
    int dflg = 0;


    TextField tx = new TextField(50);
    Button badd = new Button("         +         ");
    Button bsub = new Button("         -         ");
    Button bmult = new Button("         *         ");
    Button bdiv = new Button("         /         ");
    Button b0 = new Button("0");
    Button b1 = new Button("1");
    Button b2 = new Button("2"); 
    Button b3 = new Button("3"); 
    Button b4 = new Button("4"); 
    Button b5 = new Button("5"); 
    Button b6 = new Button("6"); 
    Button b7 = new Button("7"); 
    Button b8 = new Button("8"); 
    Button b9 = new Button("9"); 
    Button bback = new Button("Backspace"); 
    Button bclear = new Button("Clear"); 
    Button beq = new Button("=");
    Button bdot = new Button (".");

    public void init()
    {
        setLayout(null);
        setBackground(new Color (157,240,255));
        tx.setBounds(50,50,240,40);
        bback.setBounds(50,110,110,40);
        bclear.setBounds(180,110,110,40);
        b7.setBounds(50,170,50,40);
        b8.setBounds(110,170,50,40);
        b9.setBounds(170,170,50,40);
        badd.setBounds(240,170,50,40);
        b4.setBounds(50,230,50,40);
        b5.setBounds(110,230,50,40);
        b6.setBounds(170,230,50,40);
        bsub.setBounds(240,230,50,40);
        b1.setBounds(50,290,50,40);
        b2.setBounds(110,290,50,40);
        b3.setBounds(170,290,50,40);
        bmult.setBounds(240,290,50,40);
        bdot.setBounds(50,350,50,40);
        b0.setBounds(110,350,50,40);
        beq.setBounds(170,350,50,40);
        bdiv.setBounds(240,350,50,40);

        tx.setFont(new Font ("Arial",Font.BOLD,20));
        b0.setFont(new Font ("Arial",Font.BOLD,26));
        b1.setFont(new Font ("Arial",Font.BOLD,26));
        b2.setFont(new Font ("Arial",Font.BOLD,26));
        b3.setFont(new Font ("Arial",Font.BOLD,26));
        b4.setFont(new Font ("Arial",Font.BOLD,26));
        b5.setFont(new Font ("Arial",Font.BOLD,26));
        b6.setFont(new Font ("Arial",Font.BOLD,26));
        b7.setFont(new Font ("Arial",Font.BOLD,26));
        b8.setFont(new Font ("Arial",Font.BOLD,26));
        b9.setFont(new Font ("Arial",Font.BOLD,26));
        bdot.setFont(new Font ("Arial",Font.BOLD,26));
        badd.setFont(new Font ("Arial",Font.BOLD,40));
        bsub.setFont(new Font ("Arial",Font.BOLD,26));
        bmult.setFont(new Font ("Arial",Font.BOLD,26));
        bdiv.setFont(new Font ("Arial",Font.BOLD,26));
        bback.setFont(new Font ("Arial",Font.BOLD,20));
        beq.setFont(new Font ("Arial",Font.BOLD,26));
        bclear.setFont(new Font ("Arial",Font.BOLD,22));
        tx.setFont(new Font ("Arial",Font.BOLD,22));

        b0.setForeground(new Color (255,255,255));
        b1.setForeground(new Color (255,255,255));
        b2.setForeground(new Color (255,255,255));
        b3.setForeground(new Color (255,255,255));
        b4.setForeground(new Color (255,255,255));
        b5.setForeground(new Color (255,255,255));
        b6.setForeground(new Color (255,255,255));
        b7.setForeground(new Color (255,255,255));
        b8.setForeground(new Color (255,255,255));
        b9.setForeground(new Color (255,255,255));
        bback.setForeground(new Color (0,0,0));
        tx.setForeground(new Color(255,255,255));

        b0.setBackground(new Color (15,85,223));
        b1.setBackground(new Color (15,85,223));
        b2.setBackground(new Color (15,85,223));
        b3.setBackground(new Color (15,85,223));
        b4.setBackground(new Color (15,85,223));
        b5.setBackground(new Color (15,85,223));
        b6.setBackground(new Color (15,85,223));
        b7.setBackground(new Color (15,85,223));
        b8.setBackground(new Color (15,85,223));
        b9.setBackground(new Color (15,85,223));
        bback.setBackground(new Color(0,247,130));
        badd.setBackground(new Color(0,247,130));
        bsub.setBackground(new Color(0,247,130));
        bdiv.setBackground(new Color(0,247,130));
        bmult.setBackground(new Color(0,247,130));
        
        bdot.setBackground(new Color(0,247,130));
        beq.setBackground(new Color(0,247,130));
        tx.setBackground(new Color (15,85,223));

        add(tx);
        add(b0);
        add(b1);
        add(b2);
        add(b3);
        add(b4);
        add(b5);
        add(b6);
        add(b7);
        add(b8);
        add(b9);
        add(bclear);
        add(bback);
        add(beq);
        add(bdot);
        add(badd);
        add(bsub);
        add(bmult);
        add(bdiv);

        b0.addActionListener(this);
        b1.addActionListener(this);
        b2.addActionListener(this);
        b3.addActionListener(this);
        b4.addActionListener(this);
        b5.addActionListener(this);
        b6.addActionListener(this);
        b7.addActionListener(this);
        b8.addActionListener(this);
        b9.addActionListener(this);
        bback.addActionListener(this);
        bclear.addActionListener(this);
        beq.addActionListener(this);
        bdot.addActionListener(this);
        badd.addActionListener(this);
        bsub.addActionListener(this);
        bmult.addActionListener(this);
        bdiv.addActionListener(this);
    }

    public void actionPerformed(ActionEvent e)
    {
        
        
        if(e.getSource() == b0)
        {
            tx.setText(tx.getText() + "0");
        }

        if(e.getSource() == b1)
        {
            tx.setText(tx.getText() + "1");
        }

        if(e.getSource() == b2)
        {
            tx.setText(tx.getText() + "2");
        }

        if(e.getSource() == b3)
        {
            tx.setText(tx.getText() + "3");
        }

        if(e.getSource() == b4)
        {
            tx.setText(tx.getText() + "4");
        }

        if(e.getSource() == b5)
        {
            tx.setText(tx.getText() + "5");
        }

        if(e.getSource() == b6)
        {
            tx.setText(tx.getText() + "6");
        }

        if(e.getSource() == b7)
        {
            tx.setText(tx.getText() + "7");
        }

        if(e.getSource() == b8)
        {
            tx.setText(tx.getText() + "8");
        }

        if(e.getSource() == b9)
        {
            tx.setText(tx.getText() + "9");
        }

        if(e.getSource() == bdot)
        {
               if(dflg==0)
               {
                tx.setText(tx.getText() + ".");
                dflg=1;
               }
        }
        

        if(e.getSource() == badd)
        {
            dflg=0;
            if(tx.getText().length() == 0)
            {
                tx.setText("");
            }
            else
            {
                num = Double.parseDouble(tx.getText());
                tx.setText("");
                op = '+';
            }
        }

        if(e.getSource() == bsub)
        {
            dflg = 0;
            if(tx.getText().length() == 0)
            {
                tx.setText("");
            }
            else
            {
                num = Double.parseDouble(tx.getText());
                tx.setText("");
                op = '-';
            }
        }

        if(e.getSource() == bdiv)
        {
            dflg = 0;
            if(tx.getText().length() == 0)
            {
                tx.setText("");
            }
            else
            {
                num = Double.parseDouble(tx.getText());
                tx.setText("");
                op = '/';
            }
        }

        if(e.getSource() == bmult)
        {
            dflg = 0;
            if(tx.getText().length() == 0)
            {
                tx.setText("");
            }
            else
            {
                num = Double.parseDouble(tx.getText());
                tx.setText("");
                op = '*';
            }
        }

        if(e.getSource() == beq)
        {
            dflg = 0;
            if(op == '+' )
            {
                num = num + Double.parseDouble(tx.getText());
                tx.setText("" + num);
            }

            if(op == '-' )
            {
                num = num - Double.parseDouble(tx.getText());
                tx.setText("" + num);
            }

            if(op == '/' )
            {
                num = num / Double.parseDouble(tx.getText());
                tx.setText("" + num);
            }

            if(op == '*' )
            {
                num = num * Double.parseDouble(tx.getText());
                tx.setText("" + num);
            }

            tx.setText(" " + num);
        }

        if(e.getSource() == bback)
        {
            if(tx.getText().length() == 0)
            {
                tx.setText("");
            }
            else
            {
                tx.setText(tx.getText().substring(0,tx.getText().length()-1));
            }
        }

        if(e.getSource() == bclear)
        {
            tx.setText("");
        }
        
    }
}
