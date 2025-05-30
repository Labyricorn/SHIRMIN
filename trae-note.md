# SLOEACSS Console Code Structure Notes

## Main Application (`SLOEACSS-console.hta`)
- Main entry point for the HTA application
- Uses three-panel layout:
  - Header panel: Navigation and branding
  - Main content panel: Primary interface
  - Status panel: System messages
- Configured with HTA-specific settings for Windows integration

## Header Component (`header/main.htm`)
- Navigation bar with consistent styling
- CSS styling for interactive menu items:
  - Horizontal layout with floating elements
  - Visual feedback on hover
  - Consistent sizing and spacing
- Navigation sections:
  - Local system management (Connectivity, Computers, Devices)
  - Failover cluster access
  - Help and documentation

## Computer Management (`console/computers/main.htm`)
- Split-view interface design
- Two-panel layout:
  - Left panel: Computer list view
  - Right panel: Detailed computer information
- Integrated with main application frame

## Status Bar (`status/main.htm`)
- System status indicator
- Dark theme with white text for visibility
- Displays current application state
- Located at bottom of main interface

## Directory Structure
```
├── console/           # Core functionality modules
│   ├── about/        # Application information
│   ├── computers/    # Computer management interface
│   ├── connection/   # Network connectivity tools
│   ├── devices/      # Device management
│   ├── help/         # User documentation
│   └── shares/       # File sharing management
├── header/           # Navigation and branding
├── img/              # Application images and icons
└── status/           # Status display component
```

## Notes
- All HTML files use consistent commenting style
- VBScript is preferred for scripting where possible
- JavaScript used only when VBScript capabilities are insufficient
- Components are modular and loaded into main application frame