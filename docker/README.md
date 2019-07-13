README.md
# VeusCoin Docker Support
This Dockerfile builds an image that makes verusd containers.
## Notes
Figure out the port needed, and work out the command line options needed to specify the chain details. Pass those in when starting the container to get the correct peer to peer port for the chain you are working with. 

Defaults to verustest if nothing is specified.
## Example
For example, with Verus you'd want to open the peer to peer port at 27485.
## RPC Port Not So Much
If you are using ssh to access the container and running cli commands then there is no reason to open the RPC port. If you want to have remote access to the RPC port, you can open 27486 as well but this is almost always a bad idea if you're talking about real coins. 

Don't ever open the RPC port with a real wallet unless you really know what you are doing.

Mount the .komodo dir (a specific one for the container) in the container so that the wallet and details and result lasts past the lifetime of the container.

Pay attention, allowing more than 1 container to use the same wallet to stake can lose you your winnings.# username and password

### Example: VerusCoin Parameters
Standard VerusCoin parameters as a docker start command goes here.

If no username is specified on the command line then verus is used.

If no password is specified on the command line then a long default one is generated and logged once to the output log.

Both username and password can be specified on the command line when launching a container with the following command:
### Example: VerusCoin Parameters With Credentials
Standard VerusCoin parameters as a docker start command goes here. Include the username and password.v 0.0


First draft
July 13, 2019
None of this actually exists yet 
