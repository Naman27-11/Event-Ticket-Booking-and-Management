# Project Statement: Event Ticket Booking & Management System

## Problem Statement
Traditional text logs and manual bookkeeping methods used to coordinate event attendance are prone to operational lag, human typing mistakes, and database sync conflicts such as accidental overbooking. When seat allocations are adjusted manually, administrative transparency is lost and customers face long response times. 

There is a distinct need for a lightweight, stable computational system capable of handling concurrent transaction steps safely. The system must process lookups instantly, keep ticket price calculations accurate, and catch data entry faults early without causing software memory leakage or system runtime crashes.

## Scope of the Project
The scope of this project is bounded to a lightweight, console-driven in-memory booking application designed for reliable transaction validation. The system manages the lifecycle of dynamic records (including creating, reading, updating, and deleting records) using Python dictionary indexing models instead of persistent file systems or live external database servers. The codebase covers admin configuration loops, real-time availability updates, short transaction key generations, dynamic seat cancellations, and localized error trapping routines. It provides an efficient and manageable architectural model tailored specifically for university grading and validation.

## Target Users
* **Event Coordinators / Administrators:** Staff members who require clean access parameters to initialize upcoming public schedules, set baseline capacities, and monitor live seat inventory balances.
* **Ticket Consumers / General Users:** Customers who need an interactive terminal layout to query active event dates, calculate exact ticket balances, secure seat locks, and cancel transactions dynamically.

## High-Level Features
* **Isolated Administrative Gateways:** Functional functions to construct customized event properties with automated code duplicates verification.
* **Interactive Transaction Checkouts:** Core execution layer that matches customer records against current seat tracking metrics, calculates totals, and creates structural booking indexes.
* **Pseudo-Random Hashing References:** Native truncation code logic that produces short, distinct transaction identifiers to secure user records against unauthorized access.
* **Bidirectional Restoration Routines:** A logical cancellation framework that coordinates dual modifications, simultaneously dropping booking records while incrementing seating capacities.
