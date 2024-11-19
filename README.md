# Katalon-Studio-DriverPaths
A sample project showing the new DriverPath methods in Katalon Studio 10.0.0

With the update to Katalon Studio 10.0.0, the DriverFactory has been refactored for better performance. In this refactoring, the commands for DriverFactory have been changed to be browser specific. Before, in version 9.x and lower, you could call the driver path as such:

DriverFactory.getChromeDriverPath()

DriverFactory.getGeckoDriverPath()

DriverFactory.getEdgeChromiumDriverPath()

DriverFactory.getEdgeDriverPath()

In Katalon Studio 10.0.0, the drivers have been assigned their own Util class, and therefore have new methods for pulling the drivers. Here’s the updated driver methods:

Google Chrome



import com.kms.katalon.core.webui.driver.chrome.ChromeDriverUtil
String chromeDriverPath = ChromeDriverUtil.getChromeDriverPath()
Mozilla Firefox



import com.kms.katalon.core.webui.driver.firefox.FirefoxDriverUtil
String firefoxDriverPath = FirefoxDriverUtil.getDriverPath()
Microsoft Edge Chromium



import com.kms.katalon.core.webui.driver.edge.EdgeDriverUtil
String edgeChromiumDriverPath = EdgeDriverUtil.getEdgeChromiumDriverPath()
Microsoft Edge (Legacy - No Longer Supported by Microsoft)



String edgeLegacyDriverPath = EdgeDriverUtil.getEdgeDriverPath()

## Sample Project Info
In this sample project you'll find 3 test cases, for testing Chrome, Edge Chromium, and Firefox. Additionally, there is a Test Suite Collection you can run to test all 3.
