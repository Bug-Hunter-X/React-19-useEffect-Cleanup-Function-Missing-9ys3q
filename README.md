# React 19 useEffect Cleanup Function Missing

This repository demonstrates a common error in React 19 applications: forgetting to include a cleanup function in a `useEffect` hook that's functionally equivalent to `componentDidMount` in class components.  This can lead to memory leaks if not addressed.

## Problem
The `useEffect` hook without a return function (cleanup function) doesn't properly clean up resources when the component is unmounted.  This is especially problematic if the effect initializes timers, subscriptions, or other resources.

## Solution
Always include a return function in your `useEffect` hook if the effect has side effects that require cleanup when the component is unmounted.  This ensures that resources are released properly, preventing memory leaks and improving application stability.

## How to run
1. Clone this repository.
2. Navigate to the project directory in your terminal.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the application.