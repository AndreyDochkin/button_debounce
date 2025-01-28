**Key Features**:

- Simple API with edge detection
- Hardware-agnostic design
- Reusable for multiple buttons
- Configurable debounce time
- Supports both active-low and active-high buttons

**How to Use**:

1. Include both files in your project
2. Create a `Button` instance for each physical button
3. Initialize with `button_init()`
4. Regularly call `button_update()` with current state and time
5. Use the `button_just_pressed()` and `button_just_released()` for edge detection

**Configuration**:

- Set `active_state` to `LOW` for pull-up buttons
- Set `active_state` to `HIGH` for pull-down buttons
- Adjust `debounce_delay` (typically 20-100ms)

This implementation:

- Uses non-blocking timing checks
- Requires regular calls to `button_update()`
- Maintains separate state for each button
- Provides edge detection for single-press handling
- Works with any timing source (millis(), HAL ticks, etc.)
