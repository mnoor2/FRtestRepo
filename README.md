# Fetch List Display Application

This is a native Android application built using Kotlin that retrieves and displays a list of items from a JSON endpoint. The items are grouped by `listId`, sorted by both `listId` and `name`, and filtered to exclude any items with blank or null `name` values.

## Requirements
- **Android Studio**: Latest stable version
- **Build Tools**: Latest stable Android SDK
- **Minimum Android Version**: API Level 21 (Android 5.0 Lollipop)
- **Target Android Version**: Latest Android release
- **Kotlin**: 1.5+

## How to Run the Application

1. **Clone the Repository**:
   First, clone the repository from your source control tool:
   ```bash
   git clone https://github.com/mnoor2/FRtestRepo.git
   ```

2. **Open the Project in Android Studio**:
   - Launch **Android Studio** and select **Open an Existing Project**.
   - Navigate to the cloned directory and open the project.

3. **Sync Gradle**:
   - Android Studio will automatically attempt to sync the Gradle files. If it doesn’t, click **File > Sync Project with Gradle Files**.

4. **Build the Project**:
   - Ensure the project is building correctly by going to **Build > Rebuild Project**.

5. **Run the Application**:
   - Connect your Android device or start an emulator.
   - Click the **Run** button (green play icon) or press `Shift + F10` to build and run the app on the connected device/emulator.

6. **View the Results**:
   - The app will launch and fetch the JSON data.
   - Filtered and sorted items will be displayed, grouped by `listId`.
   - Each item will display its `id`, `listId`, and `name` in a scrollable list.

## Key Files and Folders
- **MainActivity.kt**: Handles the main logic of fetching and displaying the items.
- **ItemAdapter.kt**: Manages the RecyclerView’s data display, including sorting and filtering.
- **item_view.xml**: Layout file for displaying individual items in the RecyclerView.
- **AndroidManifest.xml**: Contains app permissions, including the `INTERNET` permission necessary for API calls.

## Filtering and Sorting Logic
- Items with `null` or blank `name` values are removed before being displayed.
- The remaining items are first sorted by `listId` and then by `name` (in alphabetical order).
