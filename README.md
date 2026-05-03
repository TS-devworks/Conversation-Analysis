# Ticket-Conversation-Analysis
Search Zendesk ticket conversations by keyword or phrase with powerful filtering, grouping, and export capabilities. Quickly find relevant tickets, view highlighted snippets, organize saved searches, and analyze results in a sortable, high-performance table designed for admins, managers, and senior leaders.

Ticket Conversation Analysis

A powerful Zendesk nav bar app for admins and managers to search, analyze, and export ticket conversations at scale.

Search across all ticket comments using keywords or phrases, apply advanced filters, and surface exactly the conversations you need—fast.

## Overview
####  Ticket Conversation Analysis enables deep visibility into customer interactions by letting you:

  - Search ticket conversations using comma-separated keywords or phrases
  - Instantly surface matching tickets with highlighted snippets
  - Apply multi-dimensional filtering
  - Organize and reuse searches with Saved Searches
  - Export results for reporting and analysis

Built for performance, usability, and scalability inside Zendesk.

## Key Features:
- Advanced Keyword Search
- Supports comma-separated keywords and phrases
- Executes one search per term
- Returns deduplicated ticket results
- Displays highlighted matching snippets
- Keyword Grouping (Unique Feature)
- Automatically enabled when 2+ search terms are used
#### Toggle “Group by keyword” to:
- View results grouped per keyword
- See match counts per term
- Identify overlap across terms
- Tickets matching multiple terms appear in multiple groups

## Powerful Filtering
#### Multi-select filters (server-side):
- Status
- Group
- Brand
#### Client-side filters:
- Author type
- Visibility (Public / Private)
- Date range filters
- Custom field filtering (including tagger fields)
## Results Table
- Sortable, paginated (flat mode)
- Grouped view (keyword mode)
#### Displays:
- Ticket ID (linked)
- Subject
- Assignee
- Group
- Requester info
- Status
- Channel
- Brand
- Created date
- Author type
- Visibility
- Custom field (optional)
- Highlighted snippet

## Saved Searches
- Save searches (keywords + filters) to localStorage
- Organize with custom categories
- Reload instantly
- Collapsible panel UI

#### Export:
- Export results to CSV
- Includes all visible fields and filters

#### Performance Optimizations:
- 1000 tickets per page via Search Export API
- Comment fetching stops as soon as a match is found
#### Snippet loading:
- Concurrency: 50
- Batch updates (50ms flush)
- Auto-retry (3 attempts, exponential backoff)
- Memoized filtering and regex
- Abortable in-flight searches

## Architecture
#### Single-page Zendesk nav bar app:

  - Search bar + filters
  - Results table with dual modes:
  - Flat (paginated, deduplicated)
  - Grouped by keyword (no pagination)
  - Saved searches panel
  - Parallel data fetching on mount
  
    <img width="800" height="336" alt="Ticket-Conversation-Analysis-v1 1" src="https://github.com/user-attachments/assets/b90b0420-40d0-49fc-a0b8-aca62f6d9a63" />

