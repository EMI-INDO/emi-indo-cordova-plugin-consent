# emi-indo-cordova-plugin-consent
 AdMob Consent for emi-indo-cordova-plugin-admob




https://user-images.githubusercontent.com/78555833/231193941-b58f6a7f-1de3-49e8-bb0f-7e796604e668.mp4

## Installation

```sh
cordova plugin add emi-indo-cordova-plugin-consent
```

## get Consent Request

```sh

let _getConsentRequest = () => {
    cordova.plugins.emiAdmobPlugin.getConsentRequest(
    setTagForUnderAgeOfConsent = false, // boolean
   
    (status) => { alert(status) }, 
    (error) => { alert(error)
    
    });
}

// call _getConsentRequest();

```



## consent Reset

```sh

let _consentReset = () => {
    cordova.plugins.emiAdmobPlugin.consentReset();
}

// call _consentReset();

```

# Optional
## Event | callback:
### event code

```sh
document.addEventListener('onConsentInfoUpdateSuccess', () => {

alert("on Consent Info Update Success");

});

document.addEventListener('onConsentInfoUpdateFailure', () => {

alert("on Consen Info Update Failure");

});

document.addEventListener('on.ConsentStatus.NOT_REQUIRED', () => {
// Constant Value: 1
alert("User consent not required.");

});

document.addEventListener('on.ConsentStatus.OBTAINED', () => {
// Constant Value: 3
alert("User consent obtained. Personalized vs non-personalized undefined.");

});

document.addEventListener('on.ConsentStatus.REQUIRED', () => {
// Constant Value: 2
// is Consent Form Available = the code auto, load Consent Form and consent Form show.
alert("User consent required but not yet obtained.");

});

document.addEventListener('on.ConsentStatus.UNKNOWN', () => {
//Constant Value: 0
alert("Consent status is unknown.");

});



```
