# Locators - Mechanism to locate elements within a document

In Selenium WebDriver API there is an Abstract class called By. You can make use of these methods to locate elements on the  
web page. 

public abstract class By
extends java.lang.Object

Mechanism used to locate elements within a document. In order to create your own locating mechanisms, it is possible to 
subclass this class and override the protected methods as required, though it is expected that all subclasses rely on the basic 
finding mechanisms provided through static methods of this class: 

        public WebElement findElement(WebDriver driver) 
        { 
                WebElement element = driver.findElement(By.id(getSelector())); 
                if (element == null) 
                element = driver.findElement(By.name(getSelector()); 
                return element; 
        }

Basically,there are 8 ways to locate web elements. 

1) Id: To select the element with a specified @Id attribute. Feasible for elements with fixed IDs, but not for the generated ones. 
Eg

        <input id="user" class="required" type="text"/>
        WebElement item = driver.findElement(By.id("user"));

2) Name: To select the first element with the specified @Name attribute. Feasile for elements with fixed Name,but not for the generated
ones. 
Eg

        <input id="user" name="admin" class="required" type="text"/>
        WebElement locator = driver.findElement(By.name("admin"));

3) LinkText:To select the link element which contains the matching text. 
Eg

        <a href="http://www.mywebpage.com">How to use locators?</a>
        WebElement item = driver.findElement(By.linkText("ContactUsLink"));

4) PartialLinkText
5) TagName
6) CSSSelector
7) ClassName
7) XPath 
  - Absolute XPath
  - Relative XPath
8) IdOrName




                      
     
      
     
