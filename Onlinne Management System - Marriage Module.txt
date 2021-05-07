public class Marriage
{
 Label l1,l2,l3,l4,l5,l6,l7,l8,l9,l10,l11,l12;
 Button b1,b2,b3,b4;
 public static TextField t1,t2,t4,t5,t6,t10,t12;
void main()

{

 Frame f=new Frame();
l1=new Label("Welcome To Marriage Module");
l2=new Label("Enter date of event");
l3=new Label("(DD/MM/YYYY)");
l4=new Label("No.of WallHangings");
l5=new Label("No.of Snow sprays");
l6=new Label("Catering(No.of Persons)");
l7=new Label("($10 per piece)");
l8=new Label("($50 per piece)");
l9=new Label("($35 per person)");
l10=new Label("(If orchestra is required click this button)");
l12=new Label("Total Amount");
b1=new Button("Back to home page");
b2=new Button("Calculate amount");
b3=new Button("Orchestra");
b4=new Button("Proceed to payment");
t2=new TextField();
t4=new TextField();
t5=new TextField();
t6=new TextField();
t10=new TextField();
t12=new TextField();
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
l3.setBounds(500,130,100,30);
l4.setBounds(100,160,200,30);
l5.setBounds(100,190,200,30);
l6.setBounds(100,220,200,30);
l7.setBounds(500,160,100,30);
l8.setBounds(500,190,100,30);
l9.setBounds(500,220,150,30);
l10.setBounds(500,290,400,30);
l12.setBounds(100,330,100,30);
b1.setBounds(150,400,190,30);
b2.setBounds(150,290,140,30);
b3.setBounds(350,290,140,30);
b4.setBounds(350,400,200,30);
t2.setBounds(300,130,190,30);
t4.setBounds(300,160,190,30);
t5.setBounds(300,190,190,30);
t6.setBounds(300,220,190,30);
t12.setBounds(300,330,190,30);
f.add(l1);
f.add(l2);
f.add(l3);
f.add(l4);
f.add(l5);
f.add(l6);
f.add(l7);
f.add(l8);
f.add(l9);
f.add(l10);
f.add(l12);
f.add(b1);
f.add(b2);
f.add(b3);
f.add(b4);
f.add(t2);
f.add(t4);
f.add(t5);
f.add(t6);
f.add(t10);
f.add(t12);
f.setVisible(true);
b1.addActionListener(new ActionListener() {
 public void actionPerformed(ActionEvent e)
 {

 System.out.println("Opening HomePage");
 f.setVisible(false);
 home_page hp=new home_page();
 hp.main();

 }
 });
b2.addActionListener(new ActionListener() {
 public void actionPerformed(ActionEvent e)
 {
 int a = Integer.parseInt(t4.getText());
 int b = Integer.parseInt(t5.getText());
 int c = Integer.parseInt(t6.getText());

 int f = ((a*10)+(b*50)+(c*35));
 String msg = Integer.toString(f);
 t12.setText(msg);
 }
 });
b3.addActionListener(new ActionListener() {
 public void actionPerformed(ActionEvent e)
 {
 int a = Integer.parseInt(t4.getText());
 int b = Integer.parseInt(t5.getText());
 int c = Integer.parseInt(t6.getText());

 int f = ((a*10)+(b*50)+(c*35)+1000);
 String msg = Integer.toString(f);
 t12.setText(msg);
 }
 });
b4.addActionListener(new ActionListener() {
 public void actionPerformed(ActionEvent e)
 {

 System.out.println("Opening Billing Module");
 f.setVisible(false);
 Billing1 hp=new Billing1();
 hp.main();

 }
 });
}
}