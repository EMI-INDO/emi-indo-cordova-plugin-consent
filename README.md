# DEPRECATED
- Just install emi-indo-cordova-plugin-admob
- Because UMP SDK 2.1.0 is already in emi-indo-cordova-plugin-admob

# emi-indo-cordova-plugin-consent
 AdMob Consent for [emi-indo-cordova-plugin-admob](https://github.com/EMI-INDO/emi-indo-cordova-plugin-admob)
 
## The Google User Messaging Platform ( UMP SDK 2.0.0 )




https://user-images.githubusercontent.com/78555833/231193941-b58f6a7f-1de3-49e8-bb0f-7e796604e668.mp4


## 💰Sponsor this project
  [![PayPal](https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white)](https://paypal.me/emiindo)  

## Installation

[Configure your messages under the Privacy & messaging](https://support.google.com/admob/answer/10107561)



```sh
cordova plugin add emi-indo-cordova-plugin-consent
```
```sh
cordova plugin add emi-indo-cordova-plugin-admob
```

## Remove 

```sh
cordova plugin rm emi-indo-cordova-plugin-consent
```

## get Consent Request

```sh

let _getConsentRequest = () => {
    cordova.plugins.emiAdmobPlugin.getConsentRequest(
    setTagForUnderAgeOfConsent = false, // boolean
   
    (status) => { alert(status) }, // check event code
    (error) => { alert(error)
    
    });
}

// call _getConsentRequest();

```



## consent Reset

- You should also call cordova.plugins.emiAdmobPlugin.consentReset(); if you decide to remove the UMP SDK completely from your project.

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

////////////////////////////////////////////////

// https://developers.google.com/admob/android/privacy/api/reference/com/google/android/ump/ConsentInformation.ConsentStatus

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


////////////////////////////////////////////////////////////

document.addEventListener('on.loadConsentFormError', () => {

alert("on load Consent Form Error");

});

document.addEventListener('on.ConsentFormNotAvailable', () => {

alert("on Consent Form Not Available");

});







```



