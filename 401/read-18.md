
# Many to many relationships<br>
## A Typical Example<br>

* any given employee can be assigned to multiple projects and a project may have multiple employees working for<br> it, leading to a many-to-many association between the two.<br>
* Database Setup<br>
* create the employee and project tables along with the employee_project join table with employee_id and <br>project_id as foreign keys<br>

* The Model Classes<br>
1- The model classes Employee and Project need to be created with JPA annotations<br>
2- both the Employee class and Project classes refer to one another, which means that the association between<br> them is bidirectional.<br>
3- In order to map a many-to-many association, we use the @ManyToMany, @JoinTable and @JoinColumn annotations.<br>
4- This association has two sides i.e. the owning side and the inverse side. In our example, the owning side is <br>Employee so the join table is specified on the owning side by using the @JoinTable annotation in Employee<br> class. The @JoinTable is used to define the `@join/link` table. In this case, it is <br>Employee_Project.

# Security: a humorous overview

Stories and examples from real life about security and how dangerous can it be but at the same time it is fun.<br>

Web application security is a central component of any web-based business. The global nature of the Internet <br>exposes web properties to attack from different locations and various levels of scale and complexity. Web <br>application security deals specifically with the security surrounding websites, web applications and web <br>services such as APIs.<br>

New attack vectors are constantly emerging as technology evolves. Now more than ever, comprehensive security <br>tools are needed. Previously, device endpoint protection and network security were the ultimate in <br>protective measures.
