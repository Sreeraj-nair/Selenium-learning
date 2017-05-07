## What is TestNG? 
TestNG is a testing framework designed to simplify a broad range of testing needs, from unit testing to integration testing. 

  - Write the business logic of your test and insert TestNG annotations in your code. 
  - Add the information about your test (e.g. the class name, the groups you wish to run, etc...) in a testng.xml file or in build.xml.
  - Run TestNG
  
## Annotations available in TestNG? 
@BeforeSuite: The annotated method will be run before all tests in this suite have run. 
@AfterSuite: The annotated method will be run after all tests in this suite have run. 

@BeforeTest: The annotated method will be run before any test method belonging to the classes inside the <test> tag is run. 
@AfterTest: The annotated method will be run after all the test methods belonging to the classes inside the <test> tag have run. 

@BeforeGroups: The list of groups that this configuration method will run before. This method is guaranteed to run shortly before the 
first test method that belongs to any of these groups is invoked. 
@AfterGroups: The list of groups that this configuration method will run after. This method is guaranteed to run shortly after the last 
test method that belongs to any of these groups is invoked. 

@BeforeClass: The annotated method will be run before the first test method in the current class is invoked. 
@AfterClass: The annotated method will be run after all the test methods in the current class have been run. 

@BeforeMethod: The annotated method will be run before each test method. 
@AfterMethod: The annotated method will be run after each test method.

@DataProvider: Marks a method as supplying data for a test method. The annotated method must return an Object[][] where each Object[] can be assigned the parameter list of the test method. The @Test method that wants to receive data from this DataProvider needs to use a 
dataProvider name equals to the name of this annotation.

## How to invoke TestNG? 
  - With a testng.xml file 
  - With ant 
  - From the command line

testng.xml file sample - 
   ```xml         
   <suite name="Suite1" verbose="1" >  
    <test name="Nopackage" >
        <classes>
          <class name="NoPackageTest" />
        </classes>
     </test>
 
     <test name="Regression1">
        <classes>
          <class name="test.sample.ParameterSample"/>
          <class name="test.sample.ParameterTest"/>
        </classes>
     </test>
  </suite>
  ```xml

From command line - 
   - java org.testng.TestNG testng1.xml [testng2.xml testng3.xml ...]

From eclipse 
From run.bat

## How to group tests in TestNG? 

  public class Test1 {
  @Test(groups = { "functest", "checkintest" })
  public void testMethod1() {
  }
 
  @Test(groups = {"functest", "checkintest"} )
  public void testMethod2() {
  }
 
  @Test(groups = { "functest" })
  public void testMethod3() {
  }
}

```xml
<test name="Test1">
  <groups>
    <run>
      <include name="functest"/>
    </run>
  </groups>
  <classes>
    <class name="example1.Test1"/>
  </classes>
</test>
