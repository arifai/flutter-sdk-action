# Flutter SDK Action

> [!NOTE]
> 
> This action currently only supports Android and Linux

Flutter SDK GitHub Action.

## Use Specific Flutter Shannel

```yaml
  steps:
    - name: Set up Flutter
      uses: arifai/flutter-sdk-action@v1
      with:
        channel: stable # or beta
    - run: flutter --version
```

## Build Target

### Build for Android

```yaml
  steps:
    - name: Set up Flutter
      uses: arifai/flutter-sdk-action@v1
      with:
        channel: stable
    - run: flutter pub get
    - run: flutter test
    - run: flutter build apk
```

### Build for Linux Desktop

```yaml
  steps:
    - name: Set up Flutter
      uses: arifai/flutter-sdk-action@v1
      with:
        channel: stable
    - run: flutter pub get
    - run: flutter test
    - run: flutter build linux
```