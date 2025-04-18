## 💾 QuickSave Module

The **QuickSave Module** is a lightweight utility built to instantly store and retrieve user session data, preferences, or UI state with minimal latency — perfect for real-time platforms like crypto exchanges.

### ✅ Features

- 🔹 One-click save/restore of user sessions and app state  
- 🔹 Autosave support via intervals or custom triggers  
- 🔹 Works with LocalStorage, SessionStorage, or backend APIs  
- 🔹 Easily integrates with React, Vue, or plain JavaScript  
- 🔹 Optional encryption for secure local storage

### 🔧 Use Cases

- Save open charts, selected trading pairs, or order drafts  
- Preserve form data across refreshes or accidental reloads  
- Maintain theme, layout, and filter settings between visits  
- Temporarily store bot configurations or test inputs

---

> The QuickSave Module is fully modular and can be extended or replaced depending on your application's scale or security requirements.

<script src="quicksave.min.js"></script>

import QuickSave from '@rg45/quicksave';

// Initialize QuickSave with a key
const qs = new QuickSave('user-dashboard');

// Save current state
qs.save({
  selectedPair: 'BTC/USDT',
  theme: 'dark',
  orderDraft: { type: 'limit', amount: 0.5, price: 30000 },
});

// Restore state
const previousState = qs.load();
console.log(previousState?.theme); // 'dark'

