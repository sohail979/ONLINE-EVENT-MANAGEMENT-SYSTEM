public class Billing1
{
void main()
{
 Label l1,l2,l3,l4,l5,l6,l7,l8,l9,l10,l11,l12;
 Button b1,b2,b3;
 TextField t2,t4,t5,t6,t10,t12;
 Frame f=new Frame();
l1=new Label("Welcome To Billing Module");
l2=new Label("Order ID");
l3=new Label("(DD/MM/YYYY)");
l4=new Label("Date of Event");
l5=new Label("Total Amount");
l6=new Label("Advance Amount");
b1=new Button("Confirm Payment");
b2=new Button("Modify Event");
t2=new TextField();
t4=new TextField();
t5=new TextField();
t6=new TextField();
f.addWindowListener(new WindowAdapter(){
 @Override
 public void windowClosing(WindowEvent win)
 {
 System.exit(0);
 }
 });
f.setSize(1000, 500);
f.setBackground(Color.gray);
f.setLayout(null);
l1.setBounds(100,60,190,30);
l2.setBounds(100,130,150,30);
l3.setBounds(500,160,100,30);
l4.setBounds(100,160,200,30);
l5.setBounds(100,190,200,30);
l6.setBounds(100,220,200,30);
b1.setBounds(150,290,190,30);
b2.setBounds(360,290,140,30);
t2.setBounds(300,130,190,30);
t4.setBounds(300,160,190,30);
t5.setBounds(300,190,190,30);
t6.setBounds(300,220,190,30);
f.add(l1);
f.add(l2);
f.add(l3);
f.add(l4);
f.add(l5);
f.add(l6);
f.add(b1);
f.add(b2);
f.add(t2);
f.add(t4);
f.add(t5);
f.add(t6);
f.setVisible(true);
Random ip = new Random();
int i;
i = ip.nextInt(100000);
String msg = Integer.toString(i);
t2.setText(msg);
String date=Marriage.t2.getText().toString();
String amt=Marriage.t12.getText().toString();
t4.setText(date);
t5.setText(amt);
int p = Integer.parseInt(amt);
int adv = (p*30)/100;
String s = Integer.toString(adv);
t6.setText(s);
b1.addActionListener(new ActionListener() {
 public void actionPerformed(ActionEvent e)
 {

 System.out.println("Opening HomePage");
 f.setVisible(false);
 Confirm hp=new Confirm();
 hp.main();

 }
 });
b2.addActionListener(new ActionListener() {
 public void actionPerformed(ActionEvent e)
 {

 System.out.println("Opening HomePage");
 f.setVisible(false);
 Marriage hp=new Marriage();
 hp.main();

 }
 });
}
}