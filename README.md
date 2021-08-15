# useTheme

Simple-to-use React hook to add light/dark modes to your React app.

✅️ Respects user OS preference<br />
✅️️ Respects manual theme overrides<br />
✅️ Snaps back to OS preference if needed<br />
✅️ Syncs theme across tabs and windows<br />

### Usage

1. Wrap your app in a `ThemeProvider`:

```typescript
import { ThemeProvider } from "useTheme";

ReactDOM.render(
  <React.StrictMode>
    <ThemeProvider>{/* ... Rest of your app */}</ThemeProvider>
  </React.StrictMode>,
  document.getElementById("root")
);
```

2. Use the `useTheme` hook whenever you need access to the theme:

```typescript
import { useTheme } from "useTheme";

function Component() {
  const { theme, setTheme } = useTheme();

  return (
    <div>
      Current theme: {theme}
      <button onClick={setTheme("dark")}>🌚</button>
      <button onClick={setTheme("light")}>🌝</button>
    </div>
  );
}
```
