
# SwiftUI State Management

## 1️⃣ @State – Local state within a view
- **What** → A property wrapper that stores a piece of state data inside a single SwiftUI view.  
- **Why** → Allows SwiftUI to automatically update the UI when the state changes.  
- **When** → Use when you need a **private, local piece of data** for a single view.  
- **Where** → Inside a SwiftUI view struct, declared with `@State`.  
- **Who** → Developers managing data that belongs only to one view.  

---

## 2️⃣ @Binding – Share state between parent & child views
- **What** → A property wrapper that creates a two-way connection to a `@State` variable from another view.  
- **Why** → Lets child views read and write state owned by a parent.  
- **When** → Use when you want a child view to modify a parent’s state directly.  
- **Where** → Declared in child views, connected to parent’s `@State`.  
- **Who** → Parent provides the source of truth, child gets access via `@Binding`.  

---

## 3️⃣ @ObservedObject – State from a class conforming to ObservableObject
- **What** → A property wrapper that subscribes to an external class conforming to `ObservableObject`.  
- **Why** → Lets views react to changes in shared model data.  
- **When** → Use when the data is **shared across multiple views** but not global.  
- **Where** → Inside views that need to observe an object instance.  
- **Who** → Developers structuring app with MVVM (View ↔ ViewModel).  

---

## 4️⃣ @Published – Property wrapper inside ObservableObject
- **What** → A property wrapper used inside an `ObservableObject` class to mark properties that should trigger UI updates.  
- **Why** → Makes individual properties observable for SwiftUI views.  
- **When** → Use when you want a change in a property to notify all observing views.  
- **Where** → Inside classes conforming to `ObservableObject`.  
- **Who** → Used by developers creating reactive data models.  

---

## 5️⃣ @EnvironmentObject – Share data across many views in hierarchy
- **What** → A property wrapper that injects a shared `ObservableObject` into the SwiftUI environment.  
- **Why** → Provides a way to pass data to **many views without manually passing bindings**.  
- **When** → Use when multiple unrelated views need access to the same shared data.  
- **Where** → Declared in child views that need global shared data.  
- **Who** → Developers handling app-wide or section-wide shared data.  

---

## 6️⃣ @Environment – Access system values (color scheme, locale, etc.)
- **What** → A property wrapper that lets views read values from the system environment.  
- **Why** → Allows apps to adapt automatically to system settings like Dark Mode, Locale, Accessibility.  
- **When** → Use when you want your app to follow system-level preferences.  
- **Where** → Inside a view, e.g., `@Environment(\.colorScheme) var colorScheme`.  
- **Who** → Developers who want their UI to feel natural and consistent across Apple platforms.  
