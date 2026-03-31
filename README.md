# ERC20-Snapshot-Token
ERC20 Snapshot Token
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC20/extensions/ERC20Snapshot.sol";

contract SnapToken is ERC20Snapshot {
    constructor() ERC20("SnapToken", "SNP") {
        _mint(msg.sender, 1000 ether);
    }

    function snapshot() public {
        _snapshot();
    }
}
