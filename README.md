# Sault

Flutter vault app for storing secrets: seed phrases, private keys and secure notes. Data is encrypted and stored only on the device.

## Features

- AES-256 encryption; keys kept in the device keychain (Flutter Secure Storage)
- Biometric unlock (Face ID, fingerprint)
- BIP39 seed phrase validation (12, 15, 18, 21, 24 words)
- Search, filter, activity log
- JSON export. The export is not encrypted, so handle it with care.

## Tech stack

Flutter (Dart >=3.0 <4.0), Provider, flutter_secure_storage, encrypt, local_auth, bip39

## Getting started

```bash
flutter pub get
flutter run
flutter test
```

## Project structure

```text
lib/
  models/ providers/ screens/ services/ utils/ widgets/
test/               security_flow_test.dart
docs/app-store/     privacy policy, support page, review notes
docs/plans/         UI design and implementation plans
docs/notes/         earlier design and optimization notes
stitch_vault_entry_auth/   UI mockups
```

## Security notes

- Encryption keys never leave the device keychain.
- No cloud sync.
- This app has not been independently audited.
