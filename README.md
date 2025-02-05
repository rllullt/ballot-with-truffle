# ballot-with-truffle

Ballot backed by blockchain created with the Truffle IDE as part of the Coursera Decentralized Applications Course, part of the Blockchain Specialized Program.

## Node & npm + Truffle installation

To run this dApplication, it is important to have Node v10 installed in the system.
This can be done with python virtualenv as follows (instructions for Windows):
```
python -m virtualenv env
.\env\Scripts\activate
python -m pip install nodeenv
nodeenv --python-virtualenv --node=10.24.1
npm install -g truffle@4.1.15
```

## Running the test blockchain

```
truffle develop
```

## Using the test blockchain

It is important to set the `development` variable into the truffle-config.js file, as follows:
```
module.exports = {
  networks: {
    development: {
      host: "localhost",
      port: 9545,  // RPC port for test chain provided by truffle (command `truffle develop`)
      network_id: "*",
    }
  }
}
```

## Testing

To test, it should be run the command
```
truffle test
```
