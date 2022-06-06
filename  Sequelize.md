## Sequelize 👋 👩🏻‍💻 

![seq](./assest/seq.png)
##  Associations:
Sequelize supports the standard associations: One-To-One, One-To-Many and Many-To-Many.

## Four types of associations that provides by Sequelize: 👩🏻‍🏫
* The HasOne association
* The BelongsTo association
* The HasMany association
*The BelongsToMany association<br>

1. Defining the Sequelize associations:⏭<br>
The four association types are defined in a very similar way.<br>
![seq def](./assest/seq1.png)<br>
![seq def2](./assest/seq2.png)<br>

2. Creating the standard relationships:⏭ 👩🏻‍🏫<br>
* As mentioned, usually the Sequelize associations are defined in pairs. In summary:

- To create a One-To-One relationship, the hasOne and belongsTo associations are used together;<br>
- To create a One-To-Many relationship, the hasMany and belongsTo associations are used together;<br>
- To create a Many-To-Many relationship, two belongsToMany calls are used together.<br>
* Note: there is also a Super Many-To-Many relationship, which uses six associations at once, and will be discussed in the Advanced Many-to-Many relationships guide.<br>

3. One-To-One relationships:⏭  👩🏻‍🏫 <br>
![seq](./assest/seq3.png)
![seq](./assest/seq4.png)
![seq](./assest/seq5.png)
![seq](./assest/seq6.png)
![seq](./assest/seq7.png)<br>


4. One-To-Many relationships:⏭  👩🏻‍🏫 <br>
![seq](./assest/seq8.png)
![seq](./assest/seq9.png)
![seq](./assest/seq10.png)
<br>
5. Many-To-Many relationships: ⏭  👩🏻‍🏫 <br>

* Philosophy:<br>
Many-To-Many associations connect one source with multiple targets, while all these targets can in turn be connected to other sources beyond the first.<br>
![seq](./assest/seq11.png)
![seq](./assest/seq12.png)
![seq](./assest/seq13.png)
![seq](./assest/seq14.png)

6. Basics of queries involving associations:⏭  👩🏻‍🏫 <br>
With the basics of defining associations covered, we can look at queries involving associations. The most common queries on this matter are the read queries (i.e. SELECTs). Later on, other types of queries will be shown.<br>
![seq](./assest/seq15.png)<br>

7. Creating, updating and deleting: ⏭  👩🏻‍🏫 <br>
The above showed the basics on queries for fetching data involving associations. For creating, updating and deleting, you can either:

* Use the standard model queries directly:
![seq](./assest/seq16.png)<br>

## Special methods/mixins added to instances: 👀 📝 
When an association is defined between two models, the instances of those models gain special methods to interact with their associated counterparts.

* For example, if we have two models, Foo and Bar, and they are associated, their instances will have the following methods/mixins available, depending on the association type:

1. Foo.hasOne(Bar)
2. fooInstance.getBar()
3. fooInstance.setBar()
4. fooInstance.createBar()
<br>

![seq](./assest/seq17.png) 





[Back to the main page  ✔️](README.md)