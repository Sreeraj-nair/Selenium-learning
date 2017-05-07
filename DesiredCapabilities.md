## Capabilities and DesiredCapabilities in Selenium WebDriver 

Interface Capabilities 

Implementing Class 
DesiredCapabilities, ImmutableCapabilities

### What is DesiredCapabilities? 
Every testing scenario should be executed on some specific environment. This environment can be a web browser, Mobile device, 
mobile emulator, mobile simulator and so on. 

The DesiredCapabilities class of Selenium WebDriver API helps us to tell the WebDriver, which environment the test is going 
to be executed. 

The setCapability method of DesiredCapabilities class. This is used mainly when we are executing tests on different machines in Grid 
configuration. 

The DesiredCapability is a series of key/value pairs that stores the browser properties like browserName, browserVersion, the path of 
the browserDriver in the system etc. to determine the behavior of browser at runtime. 

  - Desired capability can also be used to configure the driver instance of Selenium WebDriver.
  - We can configure driver instance like FirefoxDriver, ChromeDriver, InternetExplorerDriver by using desired capabilities.

Desired Capabilities are more useful in cases like:

  - In mobile application automation, where the browser properties and the device properties can be set.
  - In Selenium grid when we want to run the test cases on a different browser with different operating systems and versions.
  
### Methods available in DesiredCapabilities class? 

1) String browserName()
2) void setBrowserName(String browserName)
3) String setVerion()
4) void setVersion(String version)
5) Object getCapability() - to get the value of capability that is in use currently in the system. 

### Eg 
 
    import org.openqa.selenium.WebDriver;
    import org.openqa.selenium.ie.InternetExplorerDriver;
    import org.openqa.selenium.remote.DesiredCapabilities;

    public class IEtestforDesiredCapabilities {
  
      public static void main(String[] args) {

      //it is used to define IE capability 
      DesiredCapabilities capabilities = DesiredCapabilities.internetExplorer();
  
      capabilities.setCapability(CapabilityType.BROWSER_NAME, "IE");
      capabilities.setCapability(InternetExplorerDriver.
      INTRODUCE_FLAKINESS_BY_IGNORING_SECURITY_DOMAINS,true);

      System.setProperty("webdriver.ie.driver", "C:\\IEDriverServer.exe");
     //it is used to initialize the IE driver
      WebDriver driver = newInternetExplorerDriver(capabilities);
  
      driver.manage().window().maximize();

       driver.get("http://gmail.com");
  
      driver.quit();
      }
  
    }




