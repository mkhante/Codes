package p1;

public class MainClass
{
	public static void main(String[] args) 
	{
		System.out.println("---------------");
		ATM a = new ATM();
		new Person(a,100);
		new Person(a,300);
		new Person(a,400);
	}
	
}

class ATM {
	
	
	public void Withdraw(int amt)
	{
		System.out.println(" IN : "+amt);
		
		synchronized (this) 
		{
			
			try
			{
				System.out.println(" \t Open : "+amt);
				Thread.sleep((int)(Math.random()*100));
				System.out.println(" \t Close : "+amt);

			}
			catch(Exception e)
			{
				System.out.println(" Error : "+e);
			}
			

						
		}
		
		System.out.println(" OUT : "+amt);

		
	}

 }

class Person extends Thread
{
	int amt;
	ATM atm_obj;
	
	public Person(ATM a,int amt) 
	{
		atm_obj = a;
		this.amt = amt;
		start();
	}
	
	@Override
	public void run() 
	{
		try 
		{
			sleep((int)(Math.random()*100));
		} 
		catch (InterruptedException e) 
		{
			e.printStackTrace();
		}

		atm_obj.Withdraw(amt);
	}
	

}


