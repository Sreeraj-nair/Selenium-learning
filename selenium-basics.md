# Selenium-learning

## 1. What is Selenium? 
Selenium is a set of tools that automates browsers. Primarily, it is for automating web applications for testing purposes. Selenium is also the core technology in countless other browser automation tools. 

## 2. Components of Selenium 
1. Selenium IDE - a Firefox add-on that will do simple record-and-playback of interations with the browser. Can use this to create simple scripts or assist in exploratory testing.
2. Selenium WebDriver - set of APIs to create robust, browser-based regression automation suites and tests. Scale and distribute           across many environments. 
3. Selenium RC - Selenium RC is officially depricated. WebDriver is the successor of RC. 
4. Selenium Stand alone server - includes built-in grid capabilities. Can be used to scale and execute tests on different browses on       multiple OS platforms. 

## 3. Latest version of Selenium 
Selenium Stand alone server v3.4.0/WebDriver v3.4.0 

## 4. Browser drivers 
Browser drivers developed by Selenium 
1. InternetExplorer Driver server - 32 and 64 bit Windows IE. 

Third party browser drivers not developed by SeleniumHQ. 
1. Mozilla GeckoDriver 0.16.1
2. Google Chrome Driver 2.29 
3. Opera 2.27 
4. Safari Driver 
5. Appium 
6. Selendroid - Selenium for Android 
7. ios-driver 
<br/>and many more... 

## 5. Selenium Client and WebDrive Language bindings 
1. Java 
2. C# 
3. Ruby
4. Python
5. Javascript (Node)
<br/>and more...

## 6. Explicit and Implicit Waits 
Waiting is having the automated task execution elapse a certain amount of time before continuing with the next step. You should choose
to use Explicit Waits or Implicit Waits. 

Warning: Do not mix implicit and explicit waits. Doing so can cause unpredictable wait times. For eg setting an implicit wait of 10 seconds and an explicit wait of 15 seconds could cause a timeout to occur after 20 seconds. 

Explicit Waits - An explicit wait is code you define to wait for a certain condition to occur before proceeding further in the code. 
The worst case of this is Thread.sleep(), which sets the condition to an exact time period to wait.

    WebDriver driver = new FirefoxDriver();
    driver.get("http://somedomain/url_that_delays_loading");
    WebElement myDynamicElement = (new WebDriverWait(driver,10))
    .until(ExpectedConditions.presenceOfElementLocated(By.id("myDynamicElement")));
    
This waits up to 10 seconds before throwing a TimeoutException or if it finds the element will return it in 0 - 10 seconds.             WebDriverWait by default calls the ExpectedCondition every 500 milliseconds until it returns successfully. A successful return value    for the ExpectedCondition function type is a Boolean value of true, or a non-null object.

Expected Conditions - Check whether an element is Clickable (it is Displayed and Enabled)
WebDriverWait wait = new WebDriverWait(driver, 10);
WebElement element = wait.until(ExpectedConditions.elementToBeClickable(By.id("someid")));

Implicit Waits - An implicit wait is to tell the WebDriver to poll the DOM for a certain amount of time when trying to find an      
element or elements if they are no immediately available. The default setting is 0. Once set, the implicit wait is set for the life
of the WebDriver object instance. 

    WebDriver driver = new FirefoxDriver();
    driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
    driver.get("http://somedomain/url_that_delays_loading");
    WebElement myDynamicElement = driver.findElement(By.id("myDynamicElement"));


    
