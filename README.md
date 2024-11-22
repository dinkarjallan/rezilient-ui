# @dinkarjallan/rezilient-ui

A frontend library designed to enhance user experience in offline-first, resilient applications. This package provides tools and components to seamlessly bridge UI interactions with resilient application logic, ensuring a consistent and robust user experience even under challenging network conditions.

---

## What is `rezilient-ui`?

**`@dinkarjallan/rezilient-ui`** is part of the **Rezilient.js** ecosystem, focusing on UI-specific utilities for building offline-ready, network-resilient web applications. It complements **@dinkarjallan/rezilient-utils** by offering components, decorators, hooks, and HOCs tailored for UI interaction in scenarios where network conditions are unpredictable.

---

## What to Expect from This Package

- Decorators to transform UI components into service-worker managed components.
- Higher-Order Components (HOCs) to enable fallback behavior for offline scenarios.
- Hooks for managing UI state related to network conditions, offline/online mode, and sync processes.
- Prebuilt components like network status indicators, retry buttons, and sync progress bars.
- Enhanced error boundaries to gracefully handle offline-specific errors.
- Tools to simplify creating UI elements that respond dynamically to network changes.

---

## Installation

Install the package using npm or yarn:

```bash
npm install @dinkarjallan/rezilient-ui
```

or

```bash
yarn add @dinkarjallan/rezilient-ui
```

---

## Features and Examples

### 1. Decorators for Components

Easily make your components service-worker managed and offline-ready.

```javascript
import { offlineReady } from '@dinkarjallan/rezilient-ui';

@offlineReady
const DataDisplay = ({ data }) => <div>{data}</div>;
```

---

### 2. Higher-Order Components (HOCs)

Wrap your components to provide fallback behavior during offline mode.

```javascript
import { withOfflineFallback } from '@dinkarjallan/rezilient-ui';

const OfflineDisplay = withOfflineFallback(MyComponent, <FallbackUI />);
```

---

### 3. Network Status Indicators

Use prebuilt components to display real-time network status.

```javascript
import { NetworkStatusBadge } from '@dinkarjallan/rezilient-ui';

<NetworkStatusBadge />;
```

---

### 4. Retry Buttons and Prompts

Allow users to retry failed actions through intuitive UI elements.

```javascript
import { RetryButton } from '@dinkarjallan/rezilient-ui';

<RetryButton onRetry={retrySync} />;
```

---

### 5. Offline Fallback Components

Create components that adapt to offline scenarios seamlessly.

```javascript
import { OfflineAwareImage } from '@dinkarjallan/rezilient-ui';

<OfflineAwareImage src="/images/profile.jpg" />;
```

---

### 6. Hooks for UI State Management

Leverage hooks to monitor and react to network conditions.

```javascript
import { useOfflineStatus } from '@dinkarjallan/rezilient-ui';

const isOffline = useOfflineStatus();
if (isOffline) {
  alert('You are offline!');
}
```

---

### 7. Background Sync Indicators

Provide visual feedback during background syncing operations.

```javascript
import { SyncProgressBar } from '@dinkarjallan/rezilient-ui';

<SyncProgressBar />;
```

---

### 8. Enhanced Error Boundaries

Handle offline-related errors gracefully with enhanced error boundaries.

```javascript
import { OfflineErrorBoundary } from '@dinkarjallan/rezilient-ui';

<OfflineErrorBoundary fallback={<OfflinePlaceholder />}>
  <MyComponent />
</OfflineErrorBoundary>;
```

---

## Why Use `rezilient-ui`?

- **Resilient Applications:** Build robust applications that work seamlessly under poor or no network conditions.
- **Developer-Friendly API:** Leverage simple, intuitive tools to integrate offline behavior into your UI.
- **Customizable:** Extend and adapt components to suit your application's needs.
- **Part of a Unified Ecosystem:** Combine with **@dinkarjallan/rezilient-utils** to create full-stack resilient solutions.

---

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to open an issue or submit a pull request.

---

## License

This project is licensed under the [MIT License](LICENSE).
