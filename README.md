# flutter-tester

Docker image for testing flutter app in wercker

### Usage

1. Setup [wercker](https://www.wercker.com/) Pipeline.
1. Put `wercker.yml` in flutter project root.
1. Push repository.

### Sample

```wercker.yml
box:
  id: ryosms/flutter-tester
build:
  steps:
  - script:
      name: flutter upgrade
      code: |
        flutter upgrade
  - script:
      name: flutter analyze
      code: |
        flutter analyze
  - script:
      name: flutter test
      code: |
        flutter test
```