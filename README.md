# @trackpilots/single-select-date-picker

![npm](https://img.shields.io/npm/v/@trackpilots/date-picker?style=flat-square)
![license](https://img.shields.io/npm/l/@trackpilots/date-picker?style=flat-square)
![downloads](https://img.shields.io/npm/dt/@trackpilots/date-picker?style=flat-square)

A **customizable single select date picker** component built with **React** and **Tailwind CSS**.

## ✨ Screenshots  

![Screenshot](assets/screenshot-preview.png)
---

## 🚀 Installation  
You can install the package using **npm** or **yarn**:  

### **Using npm**  
```sh
npm install @trackpilots/single-select-date-picker
# or
yarn add @trackpilots/single-select-date-picker
```

Make sure Tailwind CSS is installed in your project.

##  📌 Usage
Use in Your Component
```sh
import React, { useState } from "react";
import SingleSelectDateFilter from "@trackpilots/single-select-date-picker";

const App = () => {
  const [selectedDate, setSelectedDate] = useState(null);

  const handleSelect = (date) => {
    setSelectedDate(date);
    console.log("Selected Date:", date);
  };


  return (
    <div className="p-4">
      <h2 className="text-lg font-bold">Date Picker</h2>
      <SingleSelectDateFilter
        defaultChoosenDate={"Today"}
        onSelect={handleSelect}
        selectedColor="#FF5733"
      />
      <p>Selected Date: {selectedDate ? selectedDate.toDateString() : "None"}</p>
    </div>
  );
};

export default App;
```

## 📌 DateFilter Component
A React Select component that allows users to choose a single date

## ⚙️ Props  

| Prop Name      | Type              | Default          | Description                          |
|---------------|------------------|----------------|----------------------------------|
| `selectedDate` | `Date` or `null`  | `null`         | The date of the picker. |
| `onSelect`    | `function`        | `() => {}`     | Triggered when a date is selected. |
| `selectedColor` | `string`        | `"#9D55FF"`    | Highlight color for the selected date. |
| `icon`        | `React.ElementType` | `IoCalendarOutline` | Custom calendar icon component. |
---

## **✨ Example**  
```sh
<DateFilter 
  selectedDate={new Date("2024-06-01")} 
  onSelect={(date) => console.log("User selected:", date)} 
  selectedColor="#007BFF"
/>
```

## 📦 Dependencies  

- [React](https://react.dev/)  
- [Tailwind CSS](https://tailwindcss.com/)  
- [react-icons](https://react-icons.github.io/react-icons/) (for `IoCalendarOutline` icon)  


## 📌 Maintainers
These packages are maintained by [**Quick App Studio**](https://quickappstudio.com/our-team) Developers.

##  📄 License
This project is licensed under the MIT License.