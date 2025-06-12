```bash
/**
 * Minimal Gray Rofi Configuration
 * For Arch Linux + i3wm
 */

configuration {
    modi: "drun,run,window";
    show-icons: true;
    icon-theme: "Adwaita";
    display-drun: " ";
    display-run: "󰀄";
    display-window: "";
    drun-display-format: "{name}";
    sidebar-mode: false;
    font: "Fira Code Nerd Font 12";
}

/* Gray Color Palette */
* {
    /* Gray shades */
    gray0: #1A1A1A;     /* Dark background */
    gray1: #2D2D2D;     /* Slightly lighter */
    gray2: #3D3D3D;     /* Input bar */
    gray3: #4D4D4D;     /* Borders */
    gray4: #CCCCCC;     /* Text */
    gray5: #E6E6E6;     /* Selected text */
    
    /* Application Colors */
    background: transparent;
    background-color: @gray0;
    foreground: @gray4;
    border-color: @gray3;
    selected-background: @gray3;
    selected-foreground: @gray5;
    active-background: @gray2;
    active-foreground: @gray4;
    urgent-background: #8B0000;  /* Dark red for urgent */
    urgent-foreground: @gray5;
    
    /* Spacing */
    margin: 0;
    padding: 8px;
    spacing: 4px;
    border: 0;
}

window {
    transparency: "real";
    background-color: @background-color;
    border: 0;
    border-radius: 4px;
    width: 40%;
    height: 60%;
    location: center;
}

inputbar {
    children: [prompt, entry];
    background-color: @gray2;
    border-radius: 4px;
    padding: 4px;
    border: 0;
}

prompt {
    background-color: @gray3;
    padding: 4px 8px;
    border-radius: 2px;
    text-color: @gray5;
    margin: 0 4px 0 0;
}

entry {
    padding: 4px;
    text-color: @foreground;
}

listview {
    padding: 4px 0;
    dynamic: true;
    scrollbar: false;
}

element {
    padding: 6px 8px;
    text-color: @foreground;
    border-radius: 2px;
}

element selected {
    background-color: @selected-background;
    text-color: @selected-foreground;
    border-radius: 2px;
    border: 0;
    outline: 0;
    box-shadow: none;
}

element-text {
    text-color: inherit;
}

element-icon {
    size: 32px;
    padding: 0 8px 0 0;
}
```
