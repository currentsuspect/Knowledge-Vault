
## **1. Navigation / Basic Controls**

| Shortcut                     | Action                | Notes                              |
| ---------------------------- | --------------------- | ---------------------------------- |
| `Space`                      | Play / Pause video    | Works on video tasks               |
| `←` / `→`                    | Previous / Next frame | Pixel-accurate navigation in video |
| `Ctrl + → / Ctrl + ←`        | Jump several frames   | Faster skipping                    |
| `+` / `-`                    | Zoom in / out         | Focus on details                   |
| `Mouse wheel`                | Scroll zoom           | Quick zooming while annotating     |
| `Middle mouse button + drag` | Pan canvas            | Move around without losing zoom    |

---

## **2. Annotation Creation**

|Shortcut|Action|Notes|
|---|---|---|
|`A`|Create new annotation|Usually bounding box|
|`V`|Select / Move object|Switch from creation to editing|
|`Ctrl + C`|Copy selected annotation|Use for repeated objects|
|`Ctrl + V`|Paste copied annotation|Useful across frames in video|
|`Delete`|Delete selected annotation|Be careful! No undo on video frame sometimes|
|`Shift + drag`|Constrain proportions|Keeps bounding box ratio|
|`Enter`|Finalize polygon|Use after tracing the object|
|`Esc`|Cancel current action|Handy if you misclick|

---

## **3. Editing / Adjusting**

|Shortcut|Action|Notes|
|---|---|---|
|Arrow keys|Move object 1 pixel|Super precise adjustment|
|Shift + Arrow|Move object 10 pixels|Bigger adjustments|
|Ctrl + Z|Undo|Essential to prevent errors|
|Ctrl + Y|Redo|If you undo too far|
|Alt + drag vertex|Move single polygon point|Precise polygon adjustment|
|Ctrl + drag|Duplicate annotation|Quick copy within same frame|

---

## **4. Label Management**

|Shortcut|Action|Notes|
|---|---|---|
|Tab|Switch between labels|If multiple labels are preloaded|
|Click label in sidebar|Assign to object|Faster than keyboard sometimes|
|Shift + click label|Multi-label object|Only if project allows|

---

## **5. Video-Specific Shortcuts**

|Shortcut|Action|Notes|
|---|---|---|
|`Ctrl + D`|Duplicate annotation to next frame|Time-saver for tracking moving objects|
|`Ctrl + ↑ / Ctrl + ↓`|Move annotation up/down frames|Adjust frame sequence quickly|
|`F`|Follow object|Keeps polygon/bounding box tracked over frames (if tracking enabled)|

---

## **6. Efficiency Workflow Tips**

1. **Batch similar tasks:** Annotate all “cars” first, then “people.” Muscle memory builds faster.
    
2. **Keyboard first:** Mouse for precision only. Learn `V`, `A`, `Esc`, `Enter` as second nature.
    
3. **Copy & Paste:** If a video frame repeats objects, copy annotation instead of redrawing.
    
4. **Check zoom:** Always zoom in before finalizing polygon boxes for accuracy.
    
5. **Save often:** CVAT can time out or crash. `Ctrl + S` is your friend.
    
6. **Work in bursts:** 30–50 min focused annotation → 5–10 min break. Keeps eyes and brain sharp.
    
7. **Review at the end:** A quick scroll-through ensures no missed objects or wrong labels.
    

---

## **7. Obsidian-Friendly Notes Tips**

- Make each table a separate fold (`##` or `###`) for quick reference.
    
- Highlight **must-know shortcuts** with `**bold**`.
    
- Add a daily section like:
    
  ```markdown
    ### Daily Practice
    - Memorize 3 new shortcuts
    - Annotate 50 images/videos
    - Review mistakes and adjust workflow
    ```


