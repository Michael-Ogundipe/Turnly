# Turnly
Turnly is a mobile app that allows customers to join queues remotely and helps businesses manage walk-ins and appointments efficiently in real time.

## Overview
Turnly solves the problem of wasted waiting time in businesses like salons, clinics, and service desks. Customers can join a queue remotely, see their estimated wait time, and receive notifications when they are next. Businesses can manage queues, call the next customer, and monitor daily activity—all from their admin dashboard.

## The Task

## Goal
Build a Flutter application with customer and business admin roles that demonstrates real-time queue management, notifications, and professional coding practices.

## Output

A fully functional Flutter app with:

- Role-based authentication
- Live queue updates
- Notifications
- Reusable widgets and clean architecture
- Automated tests

## Requirements

- Flutter 
- Firebase (Auth + Firestore + Cloud Messaging) 
- Riverpod for state management
- Proper folder structure with separation of concerns
- Edge case handling and loading states

## Implementation

- Role-based screens: Customer vs Business Admin
- Real-time queue updates via Firestore Realtime / Supabase Realtime
- Notifications when a customer is next
- Queue management: create session, add walk-ins, call next, mark served
- Edge case handling (cancellations, skipped entries, network errors)

## Repository Structure

```dart

lib/
  core/
    constants/
    utils/
    errors/
    theme/
  features/
    auth/
      data/
      domain/
      presentation/
    business/
      data/
      domain/
      presentation/
    queue/
      data/
      domain/
      presentation/
  shared/
    widgets/
    models/
  main.dart

```
## Critical Requirements

## Testing

- Include unit tests for queue logic (position updates, service completion)
- Include widget tests for main screens
- Test async behavior for notifications

## TRADEOFFS.md

Create a concise document (<500 words) explaining:
- **Architecture choices:** Why Riverpod and clean architecture were chosen
- **Concurrency strategy:** Sequential vs batch vs full async handling for queue updates
- **Error handling approach:** Retry, fail fast, or log & continue
- **Performance vs safety trade-offs:** What was prioritized and why
