
```java
@Test
public void wdiTest() {
        WebDriverInteractions ui = new WebDriverInteractions(driver);
        ui.browser.navigateTo("http://www.sncf.com/fr");
        ui.click(REFUSE_ALL);
        ui.set(DEPARTURE, "Paris");
        ui.click(DEPARTURE_OPTION_1);
        ui.set(ARRIVAL, "Lyon");
        ui.click(ARRIVAL_OPTION_1);
        ui.click(SEARCH);
        }
```
