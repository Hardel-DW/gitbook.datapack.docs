# Waypoint System

## <mark style="color:orange;">Overview</mark>

The **Waypoint System** allows you to mark and track specific locations in the world. Waypoints appear as colored markers visible in the world, displaying distance to each location.

---

## <mark style="color:orange;">Available Commands</mark>

### Add Waypoint

```css
/waypoint add <name> <x y z> <color>
```

Create a new waypoint at the specified coordinates.
- **name**: Any name for your waypoint
- **x y z**: Block coordinates
- **color**: Hex color (3 or 6 digits) or decimal value (0-16777215)

**Examples:**
```css
/waypoint add "Home" 100 64 200 FF0000
/waypoint add "Mine" 500 32 -300 00FF00
/waypoint add "Spawn" 0 64 0 0000FF
```

---

### Remove Waypoint

```css
/waypoint remove <name>
```

Delete a waypoint by name.

---

### List Waypoints

```css
/waypoint list
```

Display all your active waypoints with their coordinates.

---

### Clear All Waypoints

```css
/waypoint clear
```

Remove all waypoints at once.

---

## <mark style="color:orange;">Rendering</mark>

Waypoints display as:
- **Colored diamond** at the waypoint location
- **Distance text** showing how far you are
- **Pulsing border** that animates every 5 seconds
- **Smooth fading** based on distance

**Visibility Range:**
- Minimum distance: **3 blocks** (fades in)
- Maximum distance: **200 blocks** (fades out)

---

## <mark style="color:orange;">Color Format</mark>

Colors can be specified in multiple formats:
- **Hex (6 digits)**: `FF0000` (red)
- **Hex (3 digits)**: `F00` (expands to FF0000)
- **Decimal**: `16711680` (same as FF0000)

Popular colors:
- Red: `FF0000` or `255`
- Green: `00FF00` or `65280`
- Blue: `0000FF` or `255`
- Yellow: `FFFF00` or `16776960`
- White: `FFFFFF` or `16777215`

---

## <mark style="color:orange;">Status</mark>

The waypoint system is currently **command-only**. Future updates will add GUI integration and additional features!