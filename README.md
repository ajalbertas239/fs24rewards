# Check screenshot uploaded to see some of the reward files.

# Unlocking Hidden Rewards: Editing UXML Files for Debugging and Bonuses

## Introduction
If you've ever wanted to unlock hidden rewards, increase in-game currency, or gain an advantage through simple XML edits, you might be in luck. Some applications and games use `.uxml` (Unity XML) files to manage user interface components and reward data. By carefully modifying these files, you can potentially influence reward values during debugging or gameplay.

This post explores the theory behind editing `.uxml` files to alter reward values, focusing on the `debugValue` and `Value` attributes.

---

## What Are UXML Files?
UXML files are XML-based templates used in Unity's UI Toolkit. They define the structure and attributes of user interface components in a declarative manner. Within certain games or applications, these files can house valuable information, such as reward points, credits, or bonuses tied to specific actions.

## Key Areas to Target
When inspecting `.uxml` files, look for the following:

### 1. Reward Values:
```xml
<attribute appliedTo="Value" name="Value" property="textValue" debugValue="+ 50000000 500000000" noDefaultValueUpdate="true"/>
```
- The `debugValue` attribute often contains numbers that represent in-game rewards or bonus points. Increasing these values can reflect larger payouts.

### 2. Component Instances:
```xml
<UIComponent name="TileButton_Reward_Details" edition-class="Component_Instance" active="true" Title="Reward" Value="+0000" />
```
- The `Value` attribute might reflect the visual representation of rewards. Modifying it to a higher number can influence the display directly.

### 3. Dependencies:
```xml
<dependency name="Reward_Details_Content" templateId="{8daac7e5-68cc-46b5-aa20-52a192a20b50}"/>
```
- Some reward logic may reference external templates. Editing those dependencies might reveal further opportunities to adjust values.

---

## How to Edit UXML Files
1. **Locate the UXML File:**  
   - Navigate to the installation directory of the game/application. Look under UI or Component folders.

2. **Open in a Text Editor:**  
   - Use a text editor like VS Code or Notepad++ to open the file.

3. **Search for Key Terms:**  
   - Look for terms like `Value=`, `reward`, `debugValue`, or `TileButton_Reward_Details`.

4. **Modify the Values:**  
   - Increase the reward by editing the numerical values.
   ```xml
   Value="+50000000"
   ```

5. **Save and Replace:**  
   - Overwrite the original file, ensuring you back up the unedited version first.

---

## Important Considerations
- **Encoding Matters:** UXML files often use `utf-16` encoding. Ensure the edited file maintains this encoding.  
- **No Default Value Update:** The `noDefaultValueUpdate="true"` attribute ensures the value isn't overridden by the system. If absent, the game might revert the value to default.  
- **Testing:** After modifying the file, restart the application and test if the changes take effect.  

---

## Final Thoughts
Editing UXML files provides an interesting way to unlock hidden or debug features in certain games or applications. While not all software reads rewards directly from XML, many titles leave such debug values open for modification. Proceed carefully, respect the terms of service of the game/application, and always keep backups.

By exploring this technique, you might uncover hidden gems that enhance your experience or testing process. Happy modding!
