import java.io.*;
class aadhar
{
    static BufferedReader in=new BufferedReader(new InputStreamReader(System.in));
    public static void register()throws IOException
    {
        int f=1;

        FileReader fin=new FileReader("ID.txt");
        BufferedReader in1=new BufferedReader(fin);

        System.out.println("Please swipe your finger");
        String id=in.readLine();
        String preid=in1.readLine();//finding id
        while(preid!=null)
        {
            if(id.equals(preid)==true)
            {
                f=0;
                break;
            }
            preid=in1.readLine();
        }
        if(f==0)
            System.out.println("ID already registered");

        else
        {
            FileWriter fout=new FileWriter("ID.txt",true);
            PrintWriter pout=new PrintWriter(fout);
            BufferedWriter in3=new BufferedWriter(pout);
            pout.println(id);
            pout.close();
            in3.close();
            fout.close();
            pin();
            info(id);
        }
        in1.close();
    }

    public static void pin()throws IOException
    {

        FileWriter fout=new FileWriter("pin.txt",true);
        BufferedWriter bin=new BufferedWriter(fout);
        PrintWriter pout=new PrintWriter(bin);

        while(true){        
            System.out.println("Enter the pin");
            String pass1=in.readLine();
            System.out.println("\f");
            System.out.println("Re-enter the pin");
            String pass2=in.readLine();
            System.out.println("\f");

            if(pass1.equals(pass2)==true)
            {
                pout.println(pass1);
                break;
            }
            else
                System.out.println("Sorry pin does not match. Please Re-try");
        }
        pout.close();
        bin.close();
        fout.close();
    }

    public static void info(String id)throws IOException
    {
        FileWriter fout=new FileWriter(id+".txt",true);
        PrintWriter pout=new PrintWriter(fout);
        BufferedWriter in3=new BufferedWriter(pout);
        while(true)
        {
            System.out.print("Enter name : ");
            pout.println("Name : "+in.readLine());
            System.out.print("Enter DOB : ");
            pout.println("DOB  : "+in.readLine());        
            System.out.print("Enter MOB : ");
            pout.println("MOB  : "+in.readLine());
            System.out.println("1)Confirm\n2)Edit");
            int a=Integer.parseInt(in.readLine());
            if(a==1)
                break;
        }
        pout.println("Bank : ");
        pout.close();
        in3.close();
        fout.close();
    }

    public static void main(String args[])throws IOException
    {
        register();
    }
}
