# Entity relationship diagrams cheatsheet

[Official documentation](https://mermaid-js.github.io/mermaid/#/entityRelationshipDiagram) & [live editor](https://mermaid-js.github.io/mermaid-live-editor/edit#pako:eNp9kdFqwyAUhl9FznXTB8hdiTIC6xwmLRS8cXq6ypJYrCmMJO8-syVbs5V5p-f7zn_kdKCdQUgBPbXq1ataNuT7ZLui5FsmyNCv131HKHvM90wckg2lghUFSclJXe4afZ8kriNc0HhJyblSGv8l86c9zzMWWQmVVS8VkqPzEm6dP_m_UjxqtNdlztx3RPsfVLsr-gX4VbnFkrxk28jaRletWbZ9FpzusjLJNiV74OIwi9P7Z0ITlG3uWYu55xQJzhv0aGLe8tuEwApq9LWyJq6qG2sSwglrlDCKRvm3URki156NCsiMDc5DelTVBVeg2uCK90ZDGnyLMzRtfKKGDwePlnE).

## Example

```mermaid
erDiagram
Book only one--| { Author: can have Book {
string title 
string ISBN pk 
string Type 
string publisher 
string publicationYear 
string price 
string stockQuantity 
string Rating string DateAdded
}

Book } |--| { Order: Part_of Book {
}

Author
Author {
int AuthorId pk 
string Name 
string dateOfBirth 
string country
}

Customer {
int CustomerId pk 
string Name
String Email pk 
string phone 
string ShippingAddress 
string DateRegistred
}

Order many (1)--1 Customer: is_associated Order {
int ORDERid pk 
string CustomerId fk
String ISBN fk 
string ORDERDate 
int Quantity 
int subtotal
}
