import java.io.*;
class atm
{
    BufferedReader in=new BufferedReader(new InputStreamReader(System.in));
    public void enter()throws IOException
    {
        int f=0;
        String idNum;

        FileReader fin=new FileReader("ID.txt");
        BufferedReader in1=new BufferedReader(fin);

        FileReader fin1=new FileReader("pin.txt");
        BufferedReader in2=new BufferedReader(fin1);

        System.out.println("Please swipe your finger");
        String id=in.readLine();

        System.out.println("Please enter the pin");
        String pin=in.readLine();
        String e=in1.readLine();
        f=0;
        while(e!=null)
        {
            String a1=in2.readLine();
            if(id.equalsIgnoreCase(e)==true)
            {
                if(pin.equals(a1)==true)
                {
                    f=1;
                    break;
                }
            }
            e=in1.readLine();
        }
        if(f==0)
            System.out.println("Sorry,id not found");
        else 
            choose(id);
        in1.close();
        in2.close();
    }

    public void choose(String id)throws IOException
    {
        String acc[]=new String[4];
        int f=0,i=0;
        System.out.println("choose the bank");
        FileReader fin1=new FileReader(id+".txt");
        BufferedReader in2=new BufferedReader(fin1);

        String ac=in2.readLine();//multi acc
        ac=in2.readLine();
        ac=in2.readLine();
        ac=in2.readLine();
        ac=in2.readLine();
        while(ac!=null)
        {
            acc[i]=ac;
            i++;
            ac=in2.readLine();
        }

        for(int j=0;j<i;j++)
        {
            if(acc[j].equals("0000"))
                System.out.println((j+1)+" T&A BANKERS");
            else if(acc[j].equals("1111"))
                System.out.println((j+1)+" NEW GENERATION BANKING");
            else if(acc[j].equals("2222"))
                System.out.println((j+1)+" FUTURE BANKS");
        }
        i=Integer.parseInt(in.readLine());
        if(i>0&&i<5)
        {  
            i--;
            System.out.println("1) Withdraw \n2) Balance check");
            f=Integer.parseInt(in.readLine());
            if(f==1)
            {
                if(acc[i].equals("0000"))
                    I0000.transact(id);
                else if(acc[i].equals("1111"))
                    I1111.transact(id);
                else if(acc[i].equals("2222"))
                    I2222.transact(id);
            }
            else if(f==2)
            {
                if(acc[i].equals("0000"))
                    I0000.balance(id);
                else if(acc[i].equals("1111"))
                    I1111.balance(id);
                else if(acc[i].equals("2222"))
                    I2222.balance(id);
            }
            else 
                System.out.println("Wrong choice");
        }
        else
            System.out.println("Wrong choice");
        in2.close();
    }

    public static void main(String args[])throws IOException
    {
        atm atm1=new atm();
        atm1.enter();

    }
}
