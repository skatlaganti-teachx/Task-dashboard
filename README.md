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

**Location**: `src/App.jsx` - Line 33 in the `filteredTasks` logic

**Problem**: The filter comparison is incorrect - it compares `task.dueDate` with the string `'today'` instead of the actual today's date string.

### Bug 2: Mark Complete Doesn't Update UI
**Issue**: When you click "Mark Complete" or check the checkbox, the backend logs success but the UI doesn't update - the checkbox remains unchecked.

**Location**: `src/App.jsx` - Lines 41-50 in the `markComplete` function

**Problem**: The `setTasks` call that updates the UI state is commented out, so only the backend call happens.

### Bug 3: Error on Hover
**Issue**: Hovering over any task causes a silent JavaScript error in the console.

**Location**: `src/App.jsx` - Lines 54-57 in the `handleTaskHover` function

**Problem**: Trying to access `task.category.name` when `task.category` is undefined for all tasks.

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
