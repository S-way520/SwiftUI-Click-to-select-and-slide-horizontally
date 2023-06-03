# SwiftUI-Click-to-select-and-slide-horizontally
Please look at the picture.
# The first part
![IMG_0028](https://github.com/S-way520/SwiftUI-Click-to-select-and-slide-horizontally/assets/95877651/dbb0f145-ec29-46ad-905c-38ea26f1817d)
# The second part
Code file 1
```swift
import SwiftUI
@main
struct MyApp: App {
    var body: some Scene {
        WindowGroup {
            ContentView()
        }
    }
}
```
Code file 2
```swift
import SwiftUI
struct ContentView: View {
    @State private var selection = 0
    @State private var selection2 = 0
    var body: some View {
        VStack {
            
            HStack {
                Picker("", selection: $selection) {
                    Text("Tab 1").tag(0)
                    Text("Tab 2").tag(1)
                    Text("Tab 3").tag(2)
                }
                .padding()
                .pickerStyle(SegmentedPickerStyle())
                .frame(width: 200, height: 50, alignment: .center)
                Spacer()
            }
            if selection == 0 {
                HelloWorld()//An example, 一个例子
                    .frame(height: 150, alignment: .center)
            } else if selection == 1 {
                Text("This is tab 2")
                    .frame(height: 150, alignment: .center)
            } else if selection == 2 {
                Text("This is tab 3")
                    .frame(height: 150, alignment: .center)
            }
            HStack {
                Picker("", selection: $selection2) {
                    Text("Tab 1").tag(0)
                        .frame(height: 150, alignment: .center)
                    Text("Tab 2").tag(1)
                        .frame(height: 150, alignment: .center)
                    Text("Tab 3").tag(2)
                        .frame(height: 150, alignment: .center)
                }
                .padding()
                .pickerStyle(SegmentedPickerStyle())
                .frame(width: 200, height: 50, alignment: .center)
                Spacer()
            }
            if selection2 == 0 {
                Text("This is tab 1")
                    .frame(height: 150, alignment: .center)
            } else if selection2 == 1 {
                Text("This is tab 2")
                    .frame(height: 150, alignment: .center)
            } else if selection2 == 2 {
                Text("This is tab 3")
                    .frame(height: 150, alignment: .center)
            }
            Text("Button")
                .foregroundColor(.cyan)
            Spacer()
        }
    }
}
```
Code file 3
```swift
import SwiftUI
struct HelloWorld: View {
    var body: some View {
        ScrollView(.horizontal){
            HStack {
                VStack {
                    Image(systemName: "globe")
                        .imageScale(.large)
                        .foregroundColor(.accentColor)
                    Text("Hello, world!")
                }
                .padding(10)
                VStack {
                    Image(systemName: "globe")
                        .imageScale(.large)
                        .foregroundColor(.accentColor)
                    Text("Hello, Friend!")
                }
                .padding(10)
            }
        }
    }
}
```
