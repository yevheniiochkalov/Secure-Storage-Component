
# react-native-secure-storage


## Getting started

`$ npm install react-native-secure-storage --save`

or

`$ yarn add react-native-secure-storage`

### Mostly automatic installation

`$ react-native link react-native-secure-storage`


## Usage
```javascript
import SecureStorage, { ACCESS_CONTROL, ACCESSIBLE, AUTHENTICATION_TYPE } from 'react-native-secure-storage'

async() => {
  const config = {
    accessControl: ACCESS_CONTROL.BIOMETRY_ANY_OR_DEVICE_PASSCODE,
    accessible: ACCESSIBLE.WHEN_UNLOCKED,
    authenticationPrompt: 'auth with yourself',
    service: 'example',
    authenticateType: AUTHENTICATION_TYPE.BIOMETRICS,
  }
  const key = 'someKey'
  await SecureStorage.setItem(key, 'some value', config)
  const got = await SecureStorage.getItem(key, config)
  console.log(got)
}
```

