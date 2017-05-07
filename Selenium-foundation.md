## Selenium Javadoc

http://seleniumhq.github.io/selenium/docs/api/java/index.html 

## Some Packages in Selenium

    com.thoughtworks.selenium	 
    com.thoughtworks.selenium.condition	 
    com.thoughtworks.selenium.webdriven	 
    com.thoughtworks.selenium.webdriven.commands	 
    org.openqa.selenium	 
    org.openqa.selenium.chrome	 
    org.openqa.selenium.edge	
    org.openqa.selenium.firefox	 
    org.openqa.selenium.firefox.internal	 
    org.openqa.selenium.html5
    and many more... 
    
 ## What is WebDriver? 
 
 WebDriver is an interface. SearchContext is the super interface. 
 
 All Known Implementing Classes:
 ChromeDriver, EdgeDriver, EventFiringWebDriver, FirefoxDriver, InternetExplorerDriver, OperaDriver, RemoteWebDriver, SafariDriver

Important Methods: 

    |Method Name| Description | 
    ------------ ------------
    | void close()| Close the current browser window.|
    <br/>
    WebElement findElement(By by): Find the first WebElement using the given method. 
        <br/>
    java.util.List<WebElement> findElements(By by): Find all WebElements within the current page using given mechanism. 
        <br/>
    void get(String url): load a new web page in the current browser window. 
            <br/>
    String getTitle(): Get title of the current page. 
    String getWindowHandle(): Return an opaque handle to this window that uniquely identifies it within this driver instance.
    java.util.Set<java.lang.String> getWindowHandles(): Return a set of window handles which can be used to iterate over 
    all open windows of this WebDriver instance by passing them to switchTo().WebDriver.Options.window(). 
    navigate(): An abstraction allowing the driver to access browser's history and navigate to the current url. 
    WebDriver.TargetLocator switchTo(): Send future commands to a different frame or window.

## By Class? 
Direct Known Subclasses:
    By.ByClassName, By.ByCssSelector, By.ById, By.ByLinkText, By.ByName, By.ByPartialLinkText, By.ByTagName, By.ByXPath, ByAll, ByChained, ByIdOrName

