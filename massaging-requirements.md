# Massaging requirements
## Protect this house
> As a user with a shopping cart when the quantity of an item in my shopping cart is set zero then I expect that the item should be
> as if I had clicked remove from my cart.

This is a fairly simple user feature for a modern day shopping cart. If the quantity is zero that is treated the same as if the user had actually
remove the item from the cart.

When the application allowed the user to input the number 0 prior to this feature request it kept the item in the cart but it had a quantity of zero.

> As a user with a shopping cart, I may want to sell a quantity of a certain item back to the store. When I input a negative number I
> should be credited for the item and that should be reflected in the cart total.

This second use case is much more odd and can have several potential issues. What the use case is trying to allow for is a hack to allow a user
to sell their item back to the store. With this feature alone there may be several significant issues. Let's assume that we have never heard about
the desire to sell an item back to the store before. This use case is truly coming out of thin air. Furthermore, if the engineer were to implement it
as simply put as described it is very likely that this is not at all what was wanted.

It is possible that the author of the use case wanted to specify certain constraints. For instance may the price credited for those items should be
half of the current sale price. Additionally, the user may only receive a credit in the form of merchandise and not as a monetary compensation. If
this feature wasn't carefully vetted the user could simply say they are going to sell 100 of a given item, buy nothing...and receive a large credit to
their credit card and buy nothing!

## Breaking bad (requirements)
When planning a sprint it is essential to have a clear idea what the user story means as well as the implications to the integrity of the system on a
whole. What the user wants is not always the best or even correct approach. The user story needs to indicate if it is contingent upon additional
constraints or features. For instance the example of the shopping cart with the negative number relates to a whole concept of selling merchandise
back to the store. This should raise very obvious flags! Should the user be charged the full price initially and only credited when the returned
merchandise is received? If the engineer finds himself asking these questions it is imperative to enumerate the concerns, as well as the various
approaches, and limitations. At times the PO will choose (due to various pressures) to overlook the engineers best recommendation. These
matters should be well documented and the risk to move forward was deemed insignificant or not worth the possible return.

An engineer must recognize their allegiance is not only to the client but the integrity of the product on a whole. It is very likely that even after the
engineers attempts to express the possible problems that the business may simply not fully comprehend.

## The Cure
There isn't a single rock solid approach to vetting requirements. There are however, a number of techniques that can facilitate the process and
perhaps uncover a number of the seemingly hidden issues and threats.
1. What obstacle is this user story trying to overcome?
2. What or who are the different actors that are currently affected by the described scenario?
3. How will all of the actors react to the change that addresses this user story?
4. Is it possible that any of the actors affected by this change will perceive it negatively?
5. What are the upstream conditions or criteria that lead to this scenario, if applicable?
6. What are the downstream results of this change, if any?
