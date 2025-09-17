# 📱 Android 12 Splash Screen in Flutter

A step-by-step guide to set up a **custom Splash Screen** in Flutter for **Android 12 and above**, using the [`flutter_native_splash`](https://pub.dev/packages/flutter_native_splash) package.

---

## ✨ Features
- Light and Dark theme support.
- Works with Android 12+ as well as earlier versions.
- Simple configuration using a single YAML file.

---

## ⚙️ Setup Steps

### 1. Create splash images
- Design your app logo inside a **640x640** square (Radius = 320) using Figma or any design tool.
- Export two versions:
  - Light theme image
  - Dark theme image

### 2. Add images to Flutter project
Place them inside:
```
assets/images/
```

### 3. Update `pubspec.yaml`
Add your assets:
```yaml
flutter:
  assets:
    - assets/images/android_12_splash_light_theme.png
    - assets/images/android_12_splash_dark_theme.png
```

### 4. Install the package
```bash
flutter pub add flutter_native_splash
```

### 5. Create config file
In the root folder, create a file named:
```
flutter_native_splash.yaml
```

Add the following configuration:

```yaml
flutter_native_splash:
  color: "#ffffff"
  image: assets/images/android_12_splash_light_theme.png
  color_dark: "#858383"
  image_dark: assets/images/android_12_splash_dark_theme.png

  android_12:
    image: assets/images/android_12_splash_light_theme.png
    color: "#ffffff"

    image_dark: assets/images/android_12_splash_dark_theme.png
    color_dark: "#858383"
```

⚠️ **Important:** This file is very sensitive to indentation and spaces.

### 6. Generate splash screen
Run the following command:
```bash
dart run flutter_native_splash:create --path=flutter_native_splash.yaml
```

### 7. Run your app
Restart your app and you should see the new splash screen in both **Light** and **Dark** modes.

---

## 📚 References
- [Android Developers - Splash Screen API](https://developer.android.com/develop/ui/views/launch/splash-screen)  
- [YouTube Tutorial](https://www.youtube.com/watch?v=uJOuOHfAv5Y&list=PLwWuxCLlF_ucnfkI-_yNRCOTI-yJa5N-a&index=7)



## 👨‍💻 Author
**Mutee Aljabri**  
📧 Mutee1990@gmail.com  
