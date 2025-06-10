# Bugged Task Dashboard

A React dashboard built with Vite that intentionally contains several bugs for debugging practice.

## Features

- Task list with due dates and priority levels
- Filtering system (All Tasks, Pending, Completed, Due Today)
- Mark tasks as complete functionality
- Responsive design with modern UI

## Running the Application

```bash
npm install
npm run dev
```

The application will be available at `http://localhost:5173`

## Intentional Bugs 🐛

This dashboard contains **3 intentional bugs** for debugging practice:

### Bug 1: Filter Not Working
**Issue**: Clicking "Due Today" filter doesn't show any tasks, even when there are tasks due today.

### Bug 2: Mark Complete Doesn't Update UI
**Issue**: When you click "Mark Complete" or check the checkbox, the backend logs success but the UI doesn't update - the checkbox remains unchecked.

### Bug 3: Error on Hover
**Issue**: Hovering over any task causes a silent JavaScript error in the console.

## How to Debug

1. Open the browser developer tools (F12)
2. Watch the console for errors
3. Try each functionality:
   - Click different filters (especially "Due Today")
   - Try to mark tasks as complete
   - Hover over tasks and check the console

## Technologies Used

- React 18
- Vite
- Modern CSS with Flexbox
- JavaScript ES6+

## Sample Data

The dashboard includes 5 sample tasks with different due dates and priorities to test all functionality.
