# Important User Interations 

### Initializing WebDriver to Firefox

    WebDriver driver = new FirefoxDriver(); 

### Opening Firefox browser and navigating to google.com 

    driver.get("https://www.google.com"); 

### Type text in input fields
  
    WebElement messageBox = driver.findElement(By.id("commentsField")); 
    email.sendKeys("send test message"); 

### Click button 
  
    WebElement button = driver.FindElement(By.name("sbtButton")); 
    button.click(); 
  
### Mouse hover 

    Actions actions = new Actions(driver);
    WebElement mainMenu = driver.findElement(By.linkText("menulink"));
    actions.moveToElement(mainMenu);

    WebElement subMenu = driver.findElement(By.cssSelector("subLinklocator"));
    actions.moveToElement(subMenu);
    actions.click().build().perform();
  
 ### Select values from DropDown
    
    import org.openqa.selenium.support.ui.Select;
    WebElement mySelectElement = driver.findElement(By.id("mySelect"));
    Select dropdown = new Select(driver.findElement(By.id("identifier")));
    dropdown.selectByVisibleText("Italy");
    dropdown.selectByIndex(2);
    
  ### Drag and Drop 
  
    Actions action = new Actions(driver);
    action.dragAndDrop(WebElement sourceLocator, destinationLocator).build().perform();
    
    


