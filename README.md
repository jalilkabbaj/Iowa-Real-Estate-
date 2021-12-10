# Modeling the Housing Market in Ames, Iowa

### Problem Statement

The Covid pandemic has brought to light that living in spacious, modern, and tranquil homes is not a luxury but a necessity to strive as healthy and fulfilled individuals. At Black Rock hedge fund we understand that this need is reflected through many Americans. That's why we have decided to invest in the creation of spacious, affordable and long-lasting homes in certain states of the US. We have hired a team of data scientists responsible for modeling the housing market of each state in order to better evaluate our decisions. 

As a data analyst responsible for modeling the housing market in Iowa, I am tasked to investigate and evaluate the highest features that will predict sale prices. Next, I investigate what people look most in homes and make recommendations on whether or not Black Rock should invest in Iowa.


*NOTE*: This is purely a thought experiment, therefore for the sake of this project, we are not taking into consideration the time frame of this model, assuming that the data listed is fairly recent. Also I have no affiliation with Black Rock, this was used as a hypothetical situation to make this project as fun and realistic as possible. 
 
 
 ### Background Information
 “People realized they needed a place to unplug and to be alone,” she says. “They need a separate space to decompress at home, a place they could use for an at-home date night, a meditation space or a ‘crying room’ to just let out emotions alone.”
 
 “No matter what size a home is, the spaces need to work hard and respond to who lives there. It’s a different mind-set for builders to think about what’s important to consumers and what they need instead of how big a house they can build on a particular lot. Not every house needs a huge home office and a huge outdoor space.”
 
 https://www.washingtonpost.com/realestate/a-home-of-the-future-shaped-by-the-coronavirus-pandemic/2021/08/18/5e3a2032-d426-11eb-ae54-515e2f63d37d_story.html
 
 As Americans work, study, and exercise at home, they are expecting much more from their homes. “People are digging into their homes in a way that we haven’t seen since the 1950s,” says designer Patrick Mele. “People want to make their homes as singular and interesting and particular to them as they can.” They want space to exercise, and not just on a Peloton bike in the bedroom but in a light-filled room that can rival that canceled SoulCycle membership. They want a dedicated home office, and probably two, with good lighting and an elegant backdrop for a Zoom call. “The pandemic reaction is all about being inside your bubble,” says Mala Sander, an associate broker with Corcoran in the Hamptons. “You are making your bubble as beautiful and accessible as possible.”
 
 https://www.architecturaldigest.com/story/these-5-real-estate-trends-have-emerged-from-covid-19
 
This further shows that the Covid Pandemic has put people into introspection. Were people actually living in the best conditions for their well being? During quarantine we have realized how our living conditions really affected our state of mind and health. Having learned from this, Black Rock wants to accommodate people with their healthy needs in order to bring upon a better way of living.

### Data Dictionary for Engineered Features

| Feature  | Type  |  Description |
|---|---|---|
| Overall Q_C  |  int64 |  Combines the overall quality and condition of the home together |
|  1_2_floor_SF | int64  |  Combines the first and second floor square footage into one feature|
|  total bath |  int64 | Combines the half baths with the full baths into one feature  |

### Analysis and Recommendations

 This further shows that the Covid Pandemic has put people into introspection. Were people actually living in the best conditions for their well being? During quarantine we have realized how our living conditions really affected our state of mind and health. Having learned from this, Black Rock wants to accommodate people with their healthy needs in order to bring upon a better way of living



First, looking at the ridge coefficient for the continuous features, we’re able to see that living area above grade and overall quality and conditions have scored the highest. What does this mean? Looking at the area above grade feature we are able to interpret that keeping all other variables constant, a 1 square foot increase in the area above grade increases the sale price by $15,519.6. Very close to that feature is the overall condition and quality.Comparing this model to our Lasso model we are able to see similarities. Just like the ridge model the lasso model is in favor of above grade living area followed by overall quality and condition. Interpreting our above grade living area for lasso, keeping all other variables constant, a 1 square foot increase in above grade area increases the sale price by $20,677.7 . 

Both our models representing continuous coefficients are in favor of above grade area, overall quality and condition, and total basement square footage. From this information we can infer that the people in Iowa prefer having greater living area than just a spacious lot. This can be backed up by looking at our Lasso model as we are able to see that Lot Area scored the lowest in our bar chart. In fact, keeping all other variables constant, increasing Lot Area by 1 square feet increases sale price by $6,737.5 . This value is about 3 times smaller than our above grade living area, showing that the people of Iowa prefer spacious  indoor living spaces. 

Looking at the MS Zoning, we are able to see that both models are not agreeing with one another. Our ridge model puts the FV zone at the highest scoring coefficient, while our Lasso model puts the RL zones the highest scoring coefficient. Interpreting our ridge model, keep all other variables constant, a house in the FV zone increases the sale price by $2,148.60. Now Looking at our Lasso model, RL is the highest performing zone. Keeping all other variables constant, a house in the RL zone increases the sale price by $2,1178.33. Although the ridge model favors FV zones, it puts RL zones second, at a price of  $513.1019. This means that both our model agree that RL remains an important feature. 

Looking at the Year Built, we're able to see an interesting trend. What both models are closely showing is that as the year the house was built increases, so does the coefficient. Both graphs also display a peak in 2008, followed by a huge dip. In our ridge model we’re able to see that the highest scoring coefficient for the year 2008, is valued at $8,535.149. The year 2009 is valued at $3,568.990. The same can be seen in our lasso model where the highest scoring coefficient corresponds to the year 2008, and is valued at $13,337.788. The coefficient representing the year 2009 is valued at $6,412.05, showing a dip in the model. 

Next let us look at the garage type coefficient for both our models. We are able to see that both models value our garage features the same, placing the attached garage first. We can infer that because winters get cold in Iowa, people want their garage as part of their homes. This enables them to have direct access to their garage, which also serves as extra storage space. We have seen in both model, in our continuous features, that garage area plays an important role in determining price. That said having a convenient way to access garages also impacts making sale predictions. For instance in the ridge model, keeping all other variables constant, having an attached garage door increases the sale price by $6,436.79 while having a detached garage increases the sale price by $2,869. 



With that said, we can infer the following: 

People in Iowa enjoy indoor spaces.

People in Iowa want accessibility when looking for a garage.

People in Iowa enjoy living in less crowded densities.

People in Iowa look for recently built houses.

I believe that the state of Iowa is qualified for our investment, as we are looking to build spacious, tranquil, and modern homes. 





