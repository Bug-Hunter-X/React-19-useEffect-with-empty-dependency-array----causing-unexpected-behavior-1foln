# React 19 useEffect Empty Dependency Array Bug

This repository demonstrates a potential issue in React 19 related to the use of `useEffect` hooks with empty dependency arrays.  The bug arises when the component's state or props affect the effect's logic, but are not explicitly included in the dependency array.

## Bug Description

The provided `bug.jsx` file shows a simple counter component. The `useEffect` hook logs the current count after every render. While functional in basic scenarios, this pattern can lead to unexpected behavior.  If other state updates cause calculations or data fetching within the effect which depend on state or props outside of the dependencies listed, unexpected behavior can occur.

## Solution

The `bugSolution.jsx` provides a corrected version. The dependency array now includes `count`, ensuring the effect only runs when the `count` value changes. This resolves the unexpected behavior and makes the component's behavior more predictable.
