# journal

FOR JOSEPH AND JIMMY LUL XD

package introUnit;

public class Sleeper implements Runnable {

	private int number;
	private int sleepTime;
	private int sleepTime2;

	public static void main(String[] args) {
		Thread one = new Thread(new Sleeper(1));
	

		one.start();
		// while (!one.isAlive()) .isAlive() checks if thread has stopped or not
		// ;
		// (true if has not stopped, false if has stopped)
	
	}

	public Sleeper(int number) {
		this.number = number;
		this.sleepTime = (int) (5000);
		this.sleepTime2 = (int)(1000);
		
	}

	public void run() {
		try {
			System.out.println("Thread #" + number + " will sleep for " + sleepTime + "ms");
			Thread.sleep(sleepTime);

			System.out.println("Thread #" + number + " woke up");
		} catch (InterruptedException e) {
			e.printStackTrace();
		}
	}

}
