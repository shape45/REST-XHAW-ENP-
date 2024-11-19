### README: Empowering the Nation  

---

#### **Welcome to Empowering the Nation**  

Empowering the Nation was established in 2018 by Precious Radebe to provide skills training for domestic workers and gardeners in Johannesburg. The initiative supports individuals who were unable to access formal education or upskilling opportunities.  

The goal is to help domestic workers and gardeners gain marketable skills, enabling them to secure better-paying jobs or even start their own businesses.  

This project involves the development of a **web page** and a **mobile app** to:  
- Advertise the business and its training programs.  
- Receive inquiries from potential customers.  
- Provide quotes for selected services and courses.  
- Make it easy for customers to register for courses and view applicable discounts.  

---

### **Features of the Web Page and Mobile App**  

1. **Course Listings:**  
   - Six-month Learnership Programme (12 weeks).  
   - Six-week Short Skills Training Programme.  

2. **Discount Structure:**  
   - 1 Course: No discount.  
   - 2 Courses: 5% discount.  
   - 3 Courses: 10% discount.  
   - More than 3 Courses: 15% discount.  

3. **Quote Calculation:**  
   - Allows customers to select multiple courses and view the total cost after discounts.  

4. **Customer Interaction:**  
   - Inquiries: A contact form for potential customers to request information.  
   - Registration: A portal for customers to sign up for courses directly.  

5. **Admin Portal:**  
   - Manage course details.  
   - View and respond to customer inquiries.  

---

### **Technology Stack**  

- **Frontend:** HTML, CSS, JavaScript (React for interactivity).  
- **Backend:** Node.js with Express.js.  
- **Database:** MongoDB for storing customer and course information.  
- **Mobile App:** React Native for iOS and Android compatibility.  
- **Deployment:** AWS or Azure cloud hosting.  

---

### **Discount and Fee Calculation**  

Below is a sample source code in JavaScript for calculating the total fees, including discounts:  

```javascript
// Function to calculate fees with discounts
function calculateFees(coursePrices) {
    const totalCourses = coursePrices.length; // Number of courses selected
    const totalFee = coursePrices.reduce((sum, price) => sum + price, 0); // Sum of all course prices

    // Determine discount percentage based on the number of courses
    let discount = 0;
    if (totalCourses === 2) {
        discount = 0.05; // 5% discount
    } else if (totalCourses === 3) {
        discount = 0.10; // 10% discount
    } else if (totalCourses > 3) {
        discount = 0.15; // 15% discount
    }

    // Calculate final price after applying discount
    const discountedFee = totalFee - totalFee * discount;

    return {
        totalFee: totalFee.toFixed(2),       // Original fee
        discountPercentage: discount * 100, // Discount percentage
        finalFee: discountedFee.toFixed(2)  // Fee after discount
    };
}

// Example usage
const selectedCourses = [1000, 1500, 1200]; // Prices of selected courses
const result = calculateFees(selectedCourses);

console.log(`Original Fee: R${result.totalFee}`);
console.log(`Discount Applied: ${result.discountPercentage}%`);
console.log(`Final Fee: R
---

We are excited to empower more individuals with the skills they need to succeed. Together, we can build a brighter, more sustainable future!  
