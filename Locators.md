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
4) PartialLinkText: To select link (anchor tag) element which contains links matching with the specified Partial Link Text. 
Eg 

        <a href="http://www.techbeamers.com">How to use locators?</a>
        WebElement item = driver.findElement(By.PartialLinkText("ClickHere"));
5) TagName: To find element using its HTML tag. 
Eg

        List<WebElement> linkElements = driver.findElements(By.tagName("results"));
        String[] linkTexts = new String[linkElements.size()];
6) CSSSelector: To find elemet using CSS Selector. CSS Selectors are better than XPaths. Unlike, XPath they are not dependent on the DOM 
structure. They can help you perform actions which are difficult to do with XPath. 
Eg

        CSS Selector example:
        WebElement CheckElements = driver.findElements(By.cssSelector("input[id=email']"));
 
 Higlights 
 - Better and faster than XPath. 
 - More used in pages that are style centric. 
 - It's easy to define a unique CSS locator as you can combine multiple CSS attributes. 
 
 Corns 
 - It’s not easy to form a CSS selector and requires a deeper understanding of the CSS/Javascript.

7) ClassName: To find elements using CSS Class name. 
Eg

        WebElement element =driver.findElement(By.className(“sample”));
7) XPath: XPath is the perfect way of walking through the DOM structure of the web page. XPath locators are robust and reliable. 
It is one method which guarantees to locate any element on the page using the XPath expression. 

        Note*** XPath may change if there are changes in the web application. 

  - Absolute XPath
  - Relative XPath
8) IdOrName




                      
     
      
     
