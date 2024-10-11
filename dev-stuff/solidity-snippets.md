

## Contract pays to an EOA

```
address payable recipient = payable(0x123...); 
uint256 amount = 1 ether; 

bool success = recipient.send(amount);
require(success, "Failed to send Ether");

```


## Balance ...

```
_account.balance

```

## Is Contract ...


```
function isContract(address _addr) internal view returns (bool) {
    uint256 size;
    assembly {
        size := extcodesize(_addr)
    }
    return size > 0;
}

```



## Is hash 256 the same as keccak256?

For short, no. Recommendation use keccak256 (comes in various libraries).


```
function isContract(address _addr) internal view returns (bool) {
    uint256 size;
    assembly {
        size := extcodesize(_addr)
    }
    return size > 0;
}

```

### More to come...
