## Ethereum events monitor

Since there were no solutions that were well-fitted for my use case, I implemented in-house synchronization Lamda function running every 1 minute to sync the latest Ethereum transaction events for ERC-20 utility token(s). The lambda function is fetching the data from recent transaction for a given ERC-20 smart contract in order to keep the internal system up-to-date about any changes. Users are able to see those changes thanks to frequent updates and well implemented caching.

One of the use cases for the above "Ethereum events monitor" is that users get a membership tier based on the amount of tokens they own on their connnected wallet. The higher amount of tokens, the higher tier that account has, the more in-app benefits it has.

Another use case is to share the amounts to the data team, so they can put it into the data warehouse and pull out useful information for example for north star metric.

Third use case is that the solution can react to certain conditions on the chain and execute some (possibly defered) logic such as, award the users with staking rewards.

Used technologies: PostgreSQL, AWS Lambda, Infura
