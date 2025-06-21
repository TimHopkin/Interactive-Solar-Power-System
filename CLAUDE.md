# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains an **Interactive Solar Power System Diagram** - a comprehensive HTML-based visualization of a 13.5kW off-grid solar system with 19.2kWh battery storage. The project serves as both a technical diagram and a sales/educational tool for understanding solar power systems.

## Architecture

**Single-Page Application Structure:**
- **Main File**: `Original HTML.html` - Self-contained HTML document with embedded CSS and JavaScript
- **Backup File**: `Solar_Array_Diagram_Updated.html` - Copy of the updated version with SVG arrows
- **Documentation**: Comprehensive markdown files with system specifications and component details

**Key Components:**
- **Interactive Diagram**: Absolutely positioned components representing solar system parts
- **SVG Energy Flow Arrows**: Animated arrows showing power flow direction with integrated labels
- **Tooltip System**: Hover-activated detailed information for each component
- **Responsive Design**: Adapts to different screen sizes with mobile considerations
- **Clickable Components**: Direct links to supplier product pages

## Technical Implementation

**CSS Architecture:**
- Component positioning using absolute positioning within `.diagram-container`
- SVG arrows with CSS animations (`energyFlow` and `controlFlow`)
- Two arrow types: power flow (blue, solid) and control signals (teal, dashed)
- Hover effects and transitions for enhanced interactivity

**JavaScript Features:**
- Dynamic tooltip generation with component-specific data
- Click handlers for external product links
- Smooth animations and interactive effects
- Responsive behavior management

**SVG Energy Flow System:**
- Power flow arrows: Solar → DC Isolators → MPPT → Battery → DC Distribution → Inverter → House Load/Grid
- Control signal arrows: Control System ↔ Battery and Inverter communications
- Integrated text labels showing voltage/power types ("DC Power", "48V DC", "230V AC", etc.)

## Component Data Structure

The system includes detailed specifications for:
- **Solar Panels**: Canadian Solar 450W N-type TOPCon (30 units)
- **Battery System**: Pylon US5000 LiFePO4 (4 units, 19.2kWh total)
- **Inverter**: Victron MultiPlus-II 48/15000 (12kW continuous)
- **MPPT Controllers**: Victron 250V/85A (3 units)
- **Control System**: Victron Cerbo GX with Touch 50 display

## File Relationships

- `Original HTML.html` - Main interactive diagram
- `# Complete Off-Grid Solar System Guide.md` - Comprehensive system documentation
- `Product URL Quantity Unit cost Total.md` - Bill of materials with supplier links
- All files are interconnected through the HTML's tooltip system and component links

## Development Notes

**When modifying the diagram:**
- Component positioning is handled via inline styles within the SVG and component elements
- Tooltip data is stored in the `tooltipData` JavaScript object
- SVG arrows use marker definitions for arrowheads - ensure proper referencing
- Animation timing is staggered for visual flow effect

**Styling conventions:**
- Blue color scheme (#2563eb) for power flow
- Teal color scheme (#0891b2) for control signals
- Component-specific background gradients for visual hierarchy
- Consistent padding and border-radius for professional appearance

## Supplier Integration

The diagram integrates with Bimble Solar's product catalog through:
- Direct component links via `data-url` attributes
- Pricing information embedded in component details
- Tooltip system displaying technical specifications and costs
- Total system cost calculation and ROI information