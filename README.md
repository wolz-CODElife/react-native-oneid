<p style="text-align: center;">
    <a href="https://oneidtech.com">
    <img width="101" height="101" src="https://i.postimg.cc/XYwGw2WQ/One-ID-logo-Icon-PNG.png" alt="OneID" loading="lazy" /></a>
</p>

# The React Native SDK for OneID Tech

[![NPM](https://img.shields.io/npm/v/oneid-react-native.svg)](https://www.npmjs.com/package/oneid-react-native)

<p style="text-align: center;">
    A library that gives you access to OneID SSO services from your React app. <a href="https://console.oneidtech.com">Create A Developer Account Here</a>
</p>

<br>

For more information on OneID and its features, see [the documentation](https://developer.oneidtech.com).

## 📲 Installation

install the package via npm:

```bash
npm install oneid-react-native --save
```

or yarn:

```bash
yarn add oneid-react-native
```

then link the package (for react-native < 0.60):

```bash
react-native link oneid-react-native
```

## 💻 Usage:

To use the SDK, you need to import it first:

```javascript
import { OneidProvider } from "oneid-react-native";

const App = () => {
  return (
    <OneidProvider apiKey="YOUR_API_KEY">
      <YourApp />
    </OneidProvider>
  );
};
```

Then you can use the hook to login user in

```javascript
import { useOneid } from "oneid-react-native";

const YourApp = () => {
  const { login } = useOneid();

  const handleLogin = async () => {
    try {
      const user = await login();
      console.log(user);
    } catch (error) {
      console.log(error);
    }
  };

  return (
    <View>
      <Button title="Login" onPress={handleLogin} />
    </View>
  );
};
```
