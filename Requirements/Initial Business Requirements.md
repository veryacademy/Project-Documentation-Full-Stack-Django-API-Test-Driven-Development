# Initial Business and Functional Requirements

## Product Inventory Catalogue

The purpose of this document is to outline the Initial Business Requirements for the Product Inventory Catalogue system. The system will store, manage, and display product-related information for an online catalog, providing users with comprehensive details about available items, their variations, and related media. This foundational structure is essential to ensure data consistency, accuracy, and scalability as the product database grows.

In its current form, the system must accommodate a wide variety of product types — both physical and digital — while addressing specific business needs such as managing product variations, supporting multiple images for each product, and ensuring proper tracking through unique identifiers.

The key areas to address include the storage of core product information, handling of product variants, management of product images, and the organisation of product attributes and specifications. As we explore the normalisation phase, it is essential to consider how to structure this data effectively, identify potential entities, and define relationships between them to reduce redundancy and maintain data integrity.
## Common Documents:

### Business Requirements Document (BRD): 
- Focuses on the overall business goals and what the system (including the database) must accomplish.
### Functional Requirements Document (FRD): 
- Details the specific functionality and features the system must support, often with more technical detail.
### Data Requirements Specification: 
- Defines specific data elements, data types, and relationships that the database must handle.
### Entity-Relationship Diagrams (ERDs): 
- Often part of the requirements or design documentation to visually represent entities and their relationships.

# Requirements

### 1. Product Catalogue
- The system should store detailed information about products.
- Products may be **available for sale**, **discontinued**, or **temporarily unavailable**.
- Products can be either **physical** or **digital** in nature.

#### Additional Hints/Assumptions:
- Products may be organised into **categories**.
- Consider how products will be accessed via browser URLs — should we use a **human-readable slug** or a **product ID** for this purpose?

---

### 2. Product Variants
- Some products come in different **variations** (e.g., shirts in different sizes or colours).
- Each variant should have its own **price** and other attributes.

#### Additional Hints/Assumptions:
- Variants share core characteristics with the main product but differ in aspects like **size**, **color**, or **material**.
- Variants should still be recognised as versions of the **parent product**.

---

### 3. Product Images
- Products may feature multiple **images** to help customers visualise them.
- Each image should include a brief **description** (alt-text) for accessibility purposes.

#### Additional Hints/Assumptions:
- The number of images may vary between products.
- There should be a defined **order** for displaying images (e.g., primary, secondary, etc.).
- Assume that products do not share product photos.

---

### 4. Product Attributes and Specifications
- Products may have various **attributes** (e.g., color, weight, material).
- Some attributes are **universal** across products, while others are **specific** to certain product types.

#### Additional Hints/Assumptions:
- Attributes like **weight** or **dimensions** may be **numeric**, whereas others (e.g., color) may be **text-based**.
- Product attributes should be clearly defined and consistently applied.

---

### 5. Product Identifiers
- Each product should have a unique **identifier** for easy tracking and reference.
- Different products may require different identifiers, such as **SKU** or **product codes**.

#### Additional Hints/Assumptions:
- Consider whether each **product variant** should have its own unique identifier separate from the main product.
 
---

### 6. Ordering of Sub-Products or Product Lines
- Some products may consist of multiple **related product lines** (or variants) that need to be displayed in a specific **order**.

#### Additional Hints/Assumptions:
- When customers view products with multiple variants or sub-products, a **default or primary variant** should be displayed first.

---

## Summary of Key Unanswered Questions (for Students to Consider):

- What **entities** can be identified from these requirements (e.g., products, categories, types)?
- What **attributes** can be identified from the requirements (e.g., product name, product price)?
- How should relationships between entities, such as products and their categories, be structured?
- How can we efficiently manage **product variations** (e.g., size or colour)?
- What type of **identifiers** should be used for products and their variants?
- What kind of **normalisation** is required to minimise redundancy and maintain data integrity (e.g., for stock levels, product variants)?


