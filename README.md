# amazonProduct
package SeleniumTesting;

import org.openqa.selenium.By;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class AmazonProductSearch {

	public static void main(String[] args) throws InterruptedException {
		ChromeDriver driver=new ChromeDriver();
		
		driver.get("https://www.amazon.in/");
		 // Maximize the window
        driver.manage().window().maximize();
        Thread.sleep(3000);
        
        WebElement SignIn = driver.findElement(By.xpath("//span[text() = 'Hello, sign in']"));
        SignIn.click();
        Thread.sleep(3000);
        
        WebElement EmailId = driver.findElement(By.id("ap_email"));
        EmailId.click();
        
        EmailId.sendKeys("suriyaprakashravi23@gmail.com");
        EmailId.submit();
        
        WebElement Password = driver.findElement(By.id("ap_password"));
        Password.click();
        
        Password.sendKeys("Suriyaravi@23");
        Password.submit();
        Thread.sleep(3000);
        
        // Find the search bar using its name attribute
        WebElement searchBox = driver.findElement(By.name("field-keywords"));

        // Enter a search term
        searchBox.sendKeys("shoes");

        // Submit the form (this simulates hitting "Enter")
        searchBox.submit();
        
      /*  JavascriptExecutor js = (JavascriptExecutor) driver;
        for (int i = 0; i < 5; i++) { // Adjust '5' depending on how far you need to scroll
            js.executeScript("window.scrollBy(0,1000)");  // Scroll by 1000 pixels
            Thread.sleep(2000);
        
            WebElement selectProduct = driver.findElement(By.className("a-price-whole"));
            selectProduct.click();*/
        
        
        WebElement shoeSelect = driver.findElement(By.xpath("//span[text() = 'Essential Your Everyday All Purpose Walking Running Casual Shoes for Men']"));
        shoeSelect.click();
        String originalWindow = driver.getWindowHandle();
        
        Thread.sleep(4000);
       
        
        WebElement AddChart = driver.findElement(By.xpath("//span[text() = 'Add to Cart']"));
        AddChart.click();
        
        WebElement ProceedToCheckout = driver.findElement(By.xpath("//input[contains(@value,'Proceed to checkout')]"));
        ProceedToCheckout.click();
        
        
        
        

        // Wait a few seconds to view results (optional, for demo purposes)
       // try {
         //   Thread.sleep(3000);  // Wait 3 seconds
       // } catch (InterruptedException e) {
         //   e.printStackTrace();
      //  }

     //   // Close the browser
      //  driver.quit();
    }//
	}//




