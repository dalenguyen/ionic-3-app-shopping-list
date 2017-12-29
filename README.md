An Ionic 3 + Firebase Shopping List App

# Getting Started

```
npm install -g ionic cordova
```

# Install dependencies

```
npm install
npm install --only=dev
```

# Configure Firebase ENV

You need to have a firebase account, then change the name of the file: src/config/env-example.ts to env.ts with your firebase configuration info.

# Start Project

```
ionic serve
```
OR
```
ionic lab
```

# Troubleshooting

## Firebase Permission Denied

The default rules in the Firebase are:

```
{
  "rules": {
    ".read": "auth != null",
    ".write": "auth != null"
  }
}
```

You can temporary change them to:

```
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

You better set up an authenticated system for read and write databaes.
