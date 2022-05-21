# buildpackage SeliniumTest;

import java.awt.Desktop.Action;

import org.openqa.selenium.By;
import org.openqa.selenium.JavascriptExecutor;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;

public class ProjectFlipkart {
	
	//**Flipkart -Add product to cart**//
	 
	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", 
				"C:\\Users\\admin\\Downloads\\chromedriver_win32 (1)\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.get("https://www.flipkart.com/");
		Thread.sleep(2000);
		
		WebElement x =driver.findElement(By.xpath("//button[text()='✕']"));
		x.click();
		Thread.sleep(2000);
		
		WebElement login=driver.findElement(By.xpath("//a[text()='Login']"));
		login.click();
		Thread.sleep(2000);
		
		WebElement username =driver.findElement(By.xpath("(//input[@type='text'])[2]"));
		username.sendKeys("7588437879");
		Thread.sleep(2000);
		
		WebElement pass=driver.findElement(By.xpath("//input[@type='password']"));
		pass.sendKeys("7588437879");
		Thread.sleep(2000);
		
		WebElement submit=driver.findElement(By.xpath("(//button[@type='submit'])[2]"));
		submit.click(); 
		//LOGIN DONE
		
		WebElement searchbox =driver.findElement(By.xpath("//input[@type='text']"));
		searchbox.sendKeys("i phone");
		Thread.sleep(2000);
		
		Actions as =new Actions(driver);
		WebElement move =driver.findElement(By.xpath("//button[@type='submit']"));
		as.moveToElement(move).click().build().perform();
		 
	
		
	}

}
