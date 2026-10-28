# Test Cases: Customer Complaint Classification

## Objective
To evaluate how effectively different prompt designs classify customer complaints into one of four categories: Delivery, Billing, Product Quality, or Customer Service.

## Categories
- **Delivery:** Delayed, missing, or incorrectly handled deliveries.
- **Billing:** Incorrect charges, duplicate payments, or payment-related issues.
- **Product Quality:** Damaged or defective products.
- **Customer Service:** Issues involving customer support or staff.

## Test Cases

### TC01
**Complaint:** My package arrived three days later than the promised delivery date.

**Expected Category:** Delivery


### TC02
**Complaint:** I was charged twice for one order.

**Expected Category:** Billing

### TC03
**Complaint:** My headphones arrived broken, and one side does not work.

**Expected Category:** Product Quality

### TC04  
**Complaint:** I emailed customer support last week about my order, but nobody has replied.

**Expected Category:** Customer Service

### TC05 
**Complaint:** My package arrived late, and the company charged me an extra delivery fee.

**Expected Category:** Billing

### TC06   
**Complaint:** Great service! I absolutely loved being charged three times for one item.

**Expected Category:** Billing

### TC07  
**Complaint:** The package arrived on time, but the phone inside has a cracked screen.

**Expected Category:** Product Quality

### TC08  
**Complaint:** I still haven't received my order confirmation, and I don't know whether my payment went through.

**Expected Category:** Billing

## Notes
- The same eight test cases were used to evaluate all three prompt versions.
- Expected categories were defined before evaluating the model outputs.
- Complaints involving multiple issues, sarcasm, or ambiguity were included to test classification under more challenging conditions.
