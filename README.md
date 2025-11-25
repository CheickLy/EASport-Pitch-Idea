# 🏆 EA Sports Proposal: Defensive Mastermind - Pre-Snap Player Lock System

**Target Platform:** EA Sports College Football / Madden Franchise
**Proposal Date:** May 2025
**Project Lead:** [Cheick Ly]

## 📝 Project Summary

This repository contains the architecture and a specific optimization module for the **Defensive Mastermind** proposal. This feature aims to introduce a new layer of skill and control for defensive players in competitive sports titles by allowing them to set a "Pre-Snap Player Lock" with defined defensive behavior modes. The accompanying code modules demonstrate both the architectural design (`DefensiveMastermindSystem`) and practical C++ optimization (`OptimizationTASK4.h`).

---

## 🥇 1. Core Technical Skill: Data Optimization & Memory Management (`OptimizationTASK4.h`)

This module demonstrates a foundational understanding of C++ memory management, crucial for high-performance game development where resource efficiency is paramount.

### File: `OptimizationTASK4.h`

This file implements an `Inventory` class and an `Item` class, serving as a conceptual model for managing in-game assets (like player cards or virtual items).

### Key Optimization: Efficient Item Removal

The `Inventory::remove_item` method is optimized to handle the scenario where an item's quantity reaches zero after a sale (or consumption).

| Technical Action | Description | Value for Game Development |
| :--- | :--- | :--- |
| **`delete item;`** | Explicitly deallocates the memory for the `Item` object, preventing **memory leaks**. | Ensures long-running game servers and clients remain stable and resource-efficient. |
| **Array Compaction** | Shifts subsequent elements in the `Item* items[20]` array to fill the gap left by the deleted item. | Maintains a dense data structure, crucial for performance and faster subsequent lookups. |

