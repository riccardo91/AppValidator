# AppValidator

#### Import library

First of all import the library in your gradle file.
```java
compile 'com.myappfree.sdk:appvalidator:+'
```

#### Do the trick!

Add this code to your MainActivity
```java
 AppValidator.isIapToUnlock(this, new AppValidator.OnAppValidatorListener() {
            @Override
            public void validated() {
                // UNLOCK LOGIC HERE

                AppValidator.showDialog(MainActivity.this,"YOUR-CUSTOM-MESSAGE");
            }
        });
```
