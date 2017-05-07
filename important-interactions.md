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
  
