# react-complete-18-redux

## isAuthenticated state redux

## counter redux

- login and logout page loads
- split up redux slices into separate files && included in index.js store

```js
import { createSlice } from '@reduxjs/toolkit';

const initialAuthState = {
  isAuthenticated: false,
};

const authSlice = createSlice({
  name: 'auth',
  initialState: initialAuthState,
  reducers: {
    login(state) {
      state.isAuthenticated = true;
    },
    logout(state) {
      state.isAuthenticated = false;
    },
  },
});

export const authActions = authSlice.actions;
export default authSlice.reducer;
```

[Edit on StackBlitz ⚡️](https://stackblitz.com/edit/vitejs-vite-av5f2m)
