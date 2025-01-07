# React Native FlatList Blank Rendering Bug

This repository demonstrates a common React Native bug where a FlatList component renders blank even after successfully fetching data from an API.  The ActivityIndicator disappears, indicating the fetch is complete, but the list remains empty.

The `DataFetch.js` file contains the buggy code. The solution is provided in `DataFetchSolution.js`.

## Bug Description
The issue occurs because of an asynchronous operation and how React renders components. The `setData` function updates the state, but the component might rerender before the data is completely loaded causing the FlatList to not display anything.  The console might show the fetched data, but the UI remains blank.

## Solution
The solution involves carefully managing the state and using keys to effectively render items in FlatList.