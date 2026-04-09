# Tombola-Android-Internal Private Project | Architectural Showcase

Released on 11/20/2016
Offered by: Darkelly Silvestre Mota
Conctact info: Darkelly.s.m.dm@gmail.com
Android App Store: https://play.google.com/store/apps/details?id=com.gdarkelly.generator&pcampaignid=web_share

Adaptive Lottery Analysis Tool built with Java and SQLite. Implements responsive UI logic for global game formats and optimized data processing for historical draw sets.

Tombola - Advanced Lottery Strategy & Analytical Engine

🚀 Executive Summary
Tombola is a high-performance Android application designed for lottery enthusiasts and data analysts. It allows users to replicate existing global lottery formats or architect entirely new ones using a complex constraint-based engine. The app transitions from theoretical strategy planning to real-time historical data validation and "Pro Analysis" trend tracking.
________________________________________
🛠 Core Module: "Plan Your Strategy" (Constraint Engine)
The heart of Tombola is its proprietary Strategy Planner. When a user defines a primary range (1-100) and secondary range (1-100), the app initializes a multi-layered filtering system to refine potential outcomes.
Dynamic Constraint Filters
Users can apply mathematical and pattern-based rules to their plays:
•	Combinatorial Logic: Toggle "Order Matters" or "Allow Repetition."
•	Sequence Filtering: "No Allow Sequence" prevents consecutive numbers.
•	Mathematical Exclusions: Filters for Fibonacci numbers, Palindromes, Reverse numbers, and "Same Ending" patterns.
•	Proximity Rules: Exclude numbers within 2 or 10 ranges.
•	Digit-Level Filtering: A specialized "Exclude Number Containing 0-9" filter that performs string-pattern matching to eliminate specific digits from the entire pool.
•	Manual Pruning: Interactive grids allow users to individually "black-list" specific numbers from both primary and secondary pools.
________________________________________
📊 Module: History & Data Integration
The History Activity serves as the central data warehouse for the user's plays.
•	Smart Entry System: A responsive N-column input interface (supporting up to 10 columns). As users switch between a "Pick 3" and a "10-ball Keno," the UI dynamically scales ball sizes and text to maintain a perfect single-row view without clipping.
•	CSV Integration: Supports bulk-importing historical draw data via CSV, mapping external data to the internal lottery schema.
•	Bi-Directional Navigation: Historical records are hyperlinked by Date/Time. Clicking a record triggers a State-Restoration Logic that navigates the user back to the Main Activity, automatically re-loading the exact Strategy, Pick Count, and Ranges used for that specific draw.
•	Temporal Filtering: Advanced data filtering allows users to view results by 7 days, 3 months, 6 months, or custom date ranges.
________________________________________
🏆 Module: Winner Analysis & "Pro Insights"
The Winner Activity performs real-time matching between user-selected numbers and the historical database.
Visual Analytics
•	Match Highlighting: Real-time feedback where matching main numbers turn Green.
•	Special Ball Tracking: Secondary range numbers (Powerballs/Mega Balls) are treated as distinct data entities, appearing Red in history and turning Green only upon a confirmed match in the winner check.
•	Pro Analysis Dashboard: * Hot & Cold Trends: Aggregates total occurrences of selected numbers across the entire history.
o	Frequency Mapping: Displays "Match Strength" (e.g., "6x", "12x") to provide immediate insight into how often a specific number sequence appears in past draws.
________________________________________
🌍 Globalization & Localization
Tombola features a custom Internal Translation Engine (independent of standard Android OS localization). The app supports a seamless mid-session language toggle for:
•	Arabic, English, Hindi, Mandarin, Portuguese, and Spanish.
•	Engineering Note: This was implemented as a custom resource mapping feature to ensure technical lottery terminology remains accurate across diverse linguistic structures.
________________________________________
🏗 Technical Stack & Engineering Challenges
•	Language: Java (Android SDK)
•	Database: SQLite (optimized for complex relational queries between saved strategies and draw outcomes).
•	UI/UX: Responsive layouts utilizing dynamic DP scaling and StringBuilder logic for high-speed UI refreshes.
•	Architecture: State-based navigation allowing for deep-linking between historical data and strategy configurations.
