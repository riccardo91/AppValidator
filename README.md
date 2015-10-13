# AppValidator

#### Import library

First of all import the library in your gradle file.
```java
compile 'com.myappfree.sdk:appvalidator:+'
```

#### Do the trick!

Add this code to your MainActivity.
```java
 AppValidator.isIapToUnlock(this, new AppValidator.OnAppValidatorListener() {
            @Override
            public void validated() {
                // ADD YOUR UNLOCK LOGIC HERE

                AppValidator.showDialog(MainActivity.this,"YOUR-CUSTOM-MESSAGE");
            }
        });
```

Add in the *validated() block* your logic to unlock your content.

#### Testing
Add this line before *isIapToUnlock* method.

```java
     AppValidator.DEBUG = true;
```

Note: this will raise the *validated() block* every time your app is opened. Remove this line before release your app to the store.

