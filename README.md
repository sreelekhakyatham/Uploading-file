//# Uploading-file

import java.time.Duration;

import org.openqa.selenium.By;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;

public class Functional_Test_case2 {


	public static void main(String[] args) throws Exception 
	{
	FirefoxDriver driver=new FirefoxDriver();
	driver.get("https://demo.dealsdray.com/");
	driver.manage().window().maximize();
	Thread.sleep(1000);
	driver.findElement(By.xpath("//input[@name='username']")).sendKeys("prexo.mis@dealsdray.com");
	driver.findElement(By.xpath("//input[contains(@name,'password')]")).sendKeys("prexo.mis@dealsdray.com");
	driver.findElement(By.xpath("//button[@type='submit']")).click();
	driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(300));
	driver.findElement(By.xpath("(//button[contains(@tabindex,'0')])[2]")).click();
	driver.findElement(By.xpath("//button[contains(.,'PLOrders')]")).click();
	driver.findElement(By.xpath("(//button[contains(@tabindex,'0')])[6]")).click();
	driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(100));
	WebElement uploadfile = driver. findElement(By. xpath("//input[contains(@type,'file')]")); 
	uploadfile.sendKeys("\"C:\\Users\\DELL\\Downloads\\demo-data.xlsx\"");
	
	}

	

}
