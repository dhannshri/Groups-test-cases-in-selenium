# Groups-test-cases-in-selenium
Group test cases in selenium
package ui;
import org.testng.annotations.AfterClass;
import org.testng.annotations.AfterGroups;
import org.testng.annotations.AfterMethod;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeClass;
import org.testng.annotations.BeforeGroups;
import org.testng.annotations.BeforeMethod;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.Test;

import common.CommonDataSetup;
//GROUPS TEST CASES 

@Test(groups="user-registration")
public class GroupDemoTest extends CommonDataSetup {
	@BeforeClass
	public void beforeClass() {
		System.out.println("Run this Before class");
	}
	@AfterClass
	public void afterClass() {
		System.out.println("Run this after class");
	}
	
	@BeforeGroups(value="regression")
	public void beforeGroup() {
		System.out.println("Run this method before regression");
	}
	@AfterGroups(value="regression")
	public void afterGroup() {
		System.out.println("Run this method after regression");
	}
	
	
	
		@Test(priority=1,groups="regression")
		public void aTest1() {
			System.out.println("Test1");
			}
		
		@Test(priority=2,groups="regression")
		public void bTest2() {
			System.out.println("Test2");
		}
		@Test(groups={"regression","bvt"})
		public void cTest3() {
			System.out.println("Test3");
		}
		@Test(groups="bvt" )
		public void dTest4() {
			System.out.println("Test4");
		}
}
		

