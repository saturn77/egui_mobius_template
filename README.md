
<div align="center">
  <img src="assets/egui_mobius_template.png" alt="egui_mobius_template screenshot">

# egui_mobius_template

*Scaffold your GUI software design on a single surface with two sides.*

[![Version](https://img.shields.io/badge/version-0.1.0-blue)](https://github.com/saturn77/egui_mobius_template)
[![Author](https://img.shields.io/badge/author-saturn77-orange)](https://github.com/saturn77)

[![egui](https://img.shields.io/badge/egui-0.33-blue)](https://github.com/emilk/egui)
[![egui_mobius_reactive](https://img.shields.io/badge/egui__mobius__reactive-0.3.0--alpha.33-blue)](https://github.com/saturn77/egui_mobius_reactive)
[![egui_mobius_widgets](https://img.shields.io/badge/egui__mobius__widgets-0.3.0--alpha.33-blue)](https://github.com/saturn77/egui_mobius_widgets)
[![egui_dock](https://img.shields.io/badge/egui__dock-0.18.0-blue)](https://github.com/Adanos020/egui_dock)

</div>

A comprehensive collection of templates for building modern GUI applications with `egui` and `egui_mobius`. Each template demonstrates different architectural patterns to suit various application needs:

## Available Templates

### 1. Reactive Template (`examples/reactive`)
- Pure reactive architecture using `Dynamic<T>` and `Derived<T>`
- Best for: UI-focused applications with real-time state updates
- Features: Color picker, logging system, dockable panels

![alt text](assets/reactive-example.gif)

### 2. Reactive-Async Template (`examples/reactive-async`)
- Combines reactive patterns with async runtime integration
- Best for: Applications requiring background processing or I/O
- Features: All reactive features plus `MobiusRuntime` integration
![alt text](assets/reactive-async-example.gif)
### 3. Signal-Slots Template (`examples/signal-slots`)
- Event-driven architecture for heavy processing
- Best for: CPU-intensive applications, complex data processing
- Features: Signal-slot pattern for decoupled communication
![alt text](assets/signals-slots-example.gif)
A comprehensive template for building modern, reactive GUI applications with `egui` and `egui_mobius`. This template demonstrates best practices for creating responsive, thread-aware applications using the powerful features of the `egui_mobius` framework.

## Getting Started

1. Clone this template:
   ```bash
   git clone https://github.com/saturn77/egui_mobius_template.git
   cd egui_mobius_template
   ```

2. Build the examples:
   ```bash
   # Build all examples
   cargo build --examples
   ```

3. Try out the examples:
   ```bash
   # Basic reactive UI demo
   cargo run --example reactive
   
   # Async task handling demo
   cargo run --example reactive-async
   
   # RLC Circuit Simulator
   cargo run --example signals-slot
   ```

## Project Structure

```
├── src/                    # Core library code
│   └── lib.rs             # Main library interface
└── examples/
    ├── reactive/          # **Reactive** - Basic reactive UI demo
    │   ├── src/
    │   │   ├── main.rs    # Application entry
    │   │   ├── assets/    # Static resources
    │   │   └── ui/        # UI components
    │   └── README.md      # Example documentation
    ├── reactive-async/    # **Reactive-Async** sophisticated task handling demo
    │   ├── src/
    │   │   ├── main.rs    # Application entry
    │   │   ├── assets/    # Static resources
    │   │   └── ui/        # UI components
    │   └── README.md      # Example documentation
    └── signals-slot/      # **Signals-Slots** - RLC Circuit Simulator
        ├── src/
        │   ├── main.rs    # Application entry
        │   ├── circuit.rs # Circuit simulation
        │   ├── state.rs   # App state management
        │   ├── types.rs   # Data structures
        │   ├── slots/     # Signal-slot handlers
        │   └── ui/        # UI components
        └── README.md      # Example documentation
```

## Dependencies

### Core GUI Framework
- `egui` (0.33) - Immediate mode GUI framework
- `eframe` (0.33) - Framework for egui applications
- `egui_extras` (0.33) - Additional utilities and image loading support

### Mobius Framework
- `egui_mobius` (0.3.0-alpha.33) - Core reactive programming framework
- `egui_mobius_reactive` (0.3.0-alpha.33) - Reactive state management
- `egui_mobius_widgets` (0.3.0-alpha.33) - Custom widgets

### Layout & UI
- `egui_dock` (0.18.0) - Docking system for panel management
- `egui_plot` (0.34.0) - Plotting and data visualization

### Utilities
- `serde` (1.0) - Serialization for settings
- `serde_json` (1.0) - JSON support
- `once_cell` (1.19) - Static initialization
- `chrono` (0.4) - Date and time handling
- `image` (0.24) - Image loading and processing
- `dirs` (5.0) - Platform-specific directory paths

### Async & Logging
- `tokio` (1.44.1) - Async runtime with full features
- `env_logger` (0.11.7) - Logging implementation
- `log` (0.4.27) - Logging facade

### Data Processing
- `ndarray` (0.16.1) - N-dimensional arrays for numerical computing

## Contributing

This template is maintained by Saturn Rocket Company. Feel free to open issues or submit pull requests if you have suggestions for improvements.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
