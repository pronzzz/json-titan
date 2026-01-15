# JSON-Titan Advanced Features Implementation Plan

## Overview
This plan outlines the integration of Diff View, Chart Generation, and JQ Integration into the JSON-Titan single-page application. We will prioritize functionality while maintaining the "Single File" distribution goal as much as possible, though utilizing CDNs for heavy libraries (Chart.js, JQ-WASM) is necessary.

## Phase 5: Usability [Completed]
### 1. Keyboard Navigation
- **Objective**: Allow users to navigate the JSON tree using Arrow keys.
- **Status**: **Done**. Implemented with optimistic UI updates.

### 2. Export Functionality
- **Objective**: Export the current (potentially filtered) JSON to a file.
- **Status**: **Done**.

## Phase 6: Data Visualization & Diffing
### 1. Side-by-Side Diff View
- **Objective**: Compare two JSON files and highlight added/removed/changed keys.
- **UI Changes**:
  - Add "Diff Mode" toggle in Header.
  - When active, show two File Drop zones.
  - Split View: Left (Original), Right (New).
- **Worker Logic**:
  - Load two separate trees.
  - Implement a diffing algorithm (e.g., standard added/removed/modified tag).
  - Mark nodes with `diffStatus: 'added' | 'removed' | 'changed'`.
- **Rendering**:
  - Color code rows: Green (Added), Red (Removed), Yellow (Changed).
  - Sync scrolling between both views.

### 2. Chart Generation [Completed]
- **Objective**: Context-aware visualization.
- **Status**: **Done**. Implemented using Chart.js on demand.

## Phase 7: Power User Tools (JQ) [Completed]
### 1. JQ Integration
- **Objective**: Run complex queries using standard JQ syntax.
- **Status**: **Done**. Implemented with `jq-web` CDN and syntax highlighted output.

## Technical Considerations
- **CDN Dependencies**:
  - Tailwind (Already used)
  - Chart.js (for charts)
  - jq-wasm (for querying)
- **Virtual DOM**: The current custom virtual scroller is robust. We need to ensure Diff View (2x scrollers) doesn't kill performance. Sharing one `scroll` handler driving two views is best.
