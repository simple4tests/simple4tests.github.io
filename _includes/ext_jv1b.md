
```java
@Test
public void seleniumTest(){
        driver.navigate().to("http://www.sncf.com/fr");
        wait4presenceOfElementLocated(REFUSE_ALL);
        driver.findElement(REFUSE_ALL).click();
        driver.findElement(DEPARTURE).sendKeys("Paris");
        wait4presenceOfElementLocated(DEPARTURE_OPTION_1);
        driver.findElement(DEPARTURE_OPTION_1).click();
        driver.findElement(ARRIVAL).sendKeys("Lyon");
        wait4presenceOfElementLocated(ARRIVAL_OPTION_1);
        driver.findElement(ARRIVAL_OPTION_1).click();
        driver.findElement(SEARCH).click();
        }

private void wait4presenceOfElementLocated(By element){
        new FluentWait<>(driver)
        .pollingEvery(Duration.ofMillis(250))
        .withTimeout(Duration.ofSeconds(10))
        .ignoring(NoSuchElementException.class)
        .until(ExpectedConditions.presenceOfElementLocated(element));
        }
```
