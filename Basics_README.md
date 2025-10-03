
# SwiftUI Basics

## 1️⃣ SwiftUI Framework – Declarative UI framework by Apple
- **What** → A framework introduced by Apple (2019) to build UIs in a **declarative** way (you describe *what* you want, not *how*).  
- **Why** → Easier, faster, less code compared to UIKit. Updates UI automatically when data changes.  
- **When** → Use when building iOS, macOS, watchOS, and tvOS apps with modern UI.  
- **Where** → Used in Xcode with Swift. Integrated into projects targeting iOS 13+.  
- **Who** → Developers who want to build Apple ecosystem apps with modern UI principles.  

---

## 2️⃣ View Protocol – Everything on screen conforms to View
- **What** → A protocol in SwiftUI. Every UI element (`Text`, `Image`, `Button`, custom components) is a `View`.  
- **Why** → Provides a consistent structure: any UI element can be composed with others.  
- **When** → Anytime you create or use a UI element in SwiftUI.  
- **Where** → Inside your SwiftUI `structs` (e.g., `struct ContentView: View`).  
- **Who** → You, the developer, implementing your screen or component UI.  

---

## 3️⃣ Modifiers – Methods that modify views (e.g., .padding(), .background())
- **What** → Functions chained to a view to change its appearance or behavior. Example:  
  ```swift
  Text("Hello")
      .padding()
      .background(Color.yellow)
  ```  
- **Why** → Clean and readable way to apply styling & layout rules without subclassing or extra boilerplate.  
- **When** → Whenever you want to customize a view (style, position, effect).  
- **Where** → Directly after the view you want to modify.  
- **Who** → Developers use modifiers to style UI elements easily.  

---

## 4️⃣ Layout System – VStack, HStack, ZStack, LazyVStack, LazyHGrid etc.
- **What** → Containers that arrange child views in a specific order:  
  - `VStack` → Vertical  
  - `HStack` → Horizontal  
  - `ZStack` → Overlapping (layers)  
  - `LazyVStack/LazyHGrid` → Efficient lists/grids  
- **Why** → To build flexible and adaptive UIs without hardcoding positions.  
- **When** → Whenever you want to structure multiple views together.  
- **Where** → Anywhere in a SwiftUI body hierarchy.  
- **Who** → Developers use layouts to control how UI elements are arranged on screen.  

---

## 5️⃣ Preview – struct ContentView_Previews for live preview
- **What** → A special struct in SwiftUI that shows your UI in Xcode’s canvas without running the app. Example:  
  ```swift
  struct ContentView_Previews: PreviewProvider {
      static var previews: some View {
          ContentView()
      }
  }
  ```  
- **Why** → Saves time by letting you see design changes instantly.  
- **When** → During development and design iterations.  
- **Where** → At the bottom of your SwiftUI file (commonly auto-generated).  
- **Who** → Developers and designers use it to test & preview UI quickly.  
