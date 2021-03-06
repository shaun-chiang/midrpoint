# Midrpoint

A simple webpage to figure out a meeting point for up to 8 of us using the Singapore MRT.

Generated with Next.js, written in React.

Deployed at https://midrpoint.vercel.app/

## Local Setup

```
npm install
npm start
```

## Method
Given travel time estimates from MRT boards, construct an undirected weighted graph (adjacency list) with travel time as weights. Internal transfers are treated as seperate vertices (i.e. it takes time to transfer between lines).

Run Djikstra for each starting point, then calculate mean and standard deviation of each destination.

Sort results (ascending) by mean and then standard deviation.
