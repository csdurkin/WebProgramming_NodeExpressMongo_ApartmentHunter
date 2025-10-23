# WebProgramming_NodeExpressMongo_ApartmentHunter

A full-stack web application built with **Node.js**, **Express**, **MongoDB**, and **Handlebars** that streamlines the rental property search process. Apartment Hunter enables tenants to share experiences, rate landlords, and explore properties based on real community feedback. The project was developed as part of a course at Stevens Institute of Technology and was built in collaboration with the students listed here.

---

## Overview

Apartment Hunter serves as a community-driven platform where renters can:
- Search and rate **properties** and **landlords**.
- Create **user profiles** as tenants or landlords.
- Participate in a **community forum**.
- Flag inappropriate content through a **moderation system**.

The application emphasizes transparency, accountability, and tenant empowerment.

---

## Key Featuresw

1. **Property Listings and Ratings**  
   - Tenants can view, add, and review properties.  
   - Each listing includes location details, property type, and average ratings across multiple criteria.

2. **Landlord Profiles and Reviews**  
   - Landlords have profiles with associated properties and cumulative ratings.  
   - Tenants can provide written reviews and quantitative feedback.

3. **Tenant and Landlord Accounts**  
   - Users register as tenants or landlords.  
   - Tenants can favorite listings and contribute reviews.

4. **Community Forum**  
   - Provides discussion threads and comment replies.  
   - Encourages users to share rental advice and local experiences.

5. **Moderation and Reporting System**  
   - Built-in mechanism for reporting inappropriate content.  
   - Administrators can manage flagged content.

6. **Search Functionality**  
   - Text-based search for properties, landlords, and forum topics.
   - Google Maps API integration for spatial property discovery.

---

## Technical Stack

| Layer | Technology |
|-------|-------------|
| Frontend | Handlebars.js, Bootstrap 3 |
| Backend | Node.js, Express.js |
| Database | MongoDB |
| Authentication | express-session, bcrypt/bcryptjs |
| Security | Input validation, XSS filtering (xss), sessions |
| Mapping | Google Maps JavaScript API |

---

## File Layout

```
project/
├── app.js                     # Express app setup and middleware
├── seed.js                    # Populates MongoDB with initial users, landlords, and properties
├── package.json               # Dependencies and run scripts
├── config/                    # MongoDB connection setup
├── data/                      # Data layer for properties, users, threads
├── routes/                    # Express route controllers
├── views/                     # Handlebars templates
├── public/                    # CSS, JS, and static assets
├── helper.js                  # Utility helpers
└── middleware.js              # Authentication middleware
```

---

## Setup Instructions

1. **Clone Repository**  
   ```bash
   git clone https://github.com/csdurkin/CS546_group_18.git
   cd CS546_group_18
   ```

2. **Install Dependencies**  
   ```bash
   npm install
   ```

3. **Seed the Database**  
   ```bash
   npm run seed
   ```

4. **Start the Server**  
   ```bash
   npm start
   ```
   The app runs at **http://localhost:3000**.

---

## Seed Data and Default Accounts

To simplify testing, the following users are preloaded via `seed.js`:

| Role | Username | Password |
|------|-----------|-----------|
| Admin | johndoeki | Connor123@ |
| Landlord | rajesha | Connor123@ |
| Tenant | johndoek | Connor123@ |

---

## Security and Validation

- Input validation implemented across **client**, **routes**, and **database functions**.
- **XSS sanitization** via the `xss` library.
- **Session-based authentication** using `express-session`.
- Passwords securely stored using **bcrypt hashing**.

---

## Known Issues

- Google Maps may not render properly in Microsoft Edge.
- Certain duplicate Handlebars configurations in `app.js` should be refactored.
- Concurrent review submissions may cause rating sync delays.

---

## Future Improvements

- Enhanced moderation dashboard for admins.
- Expanded geolocation features and filtering.
- Full Jest/Supertest integration for automated testing.

---

## Author

Connor S. Durkin 

#Additonal Authors
Arya Shah
Jayanth Kanala 
Gnaneswar Koyalamoodi 
