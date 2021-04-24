<style>
img[src*='#center'] { 
    display: block;
    margin: auto;
}
</style>
# SHIPS - Protocol Spec

### Terminology
- **SHPS** - A protocol token used to govern the ecosystem, staking the protocol token will result in % of yield extracted from proceeds from Release Token Sales
- **Release Tokens** - Tokens issued by developers that correspond to a feature release of a project it does not have to parallel semantic releases
- **Semantic Release** - Developers have a release schedule that often includes the format major.minor.patch ex. 1.0.2 this corresponds to features and bug release according to things as they appear
- **Feature Release** - Developers have the ability to tag releases as corresponding to a group. For instance a feature release may include x number  of Semantic Releases and be called a logical name such as Prickly Hedgehog.
- **Token Release Minting Event** - A minting occurs at the developers discretion according to the Feature Release Schedule, there may be multiple minting events for a single feature release. A short term cap on supply with more issues being made as time progresses.

- **Feature Release Schedule** - A release schedule set on creation of a feature release. It says there will be x number of Minting Events, before the release will be considered closed.   

- **Token Release Close Event** - A token close event happens when the Feature Release Schedule is complete. This signals the closing of release.
- **Feature Release NFT** - A feature release NFT is reedemable when an event closes any majority token holder is able to then use the release tokens to mint the NFT and become the owner of the release.
- **Project** - A project is used to refer to a singe software entity. For example Near-CLI is a project, that is composed of feature releases, that is composed of semantic releases.
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

### Project Lifecycle 
![release-token-lifecycle](https://user-images.githubusercontent.com/173187/114090955-ecb35e00-986c-11eb-9d73-813efdf09fd5.png)
1. Here the  project lifecycle begins with the developer setting a release schedule
2. Then tags a semantic release as a milestone mile marker for the Feature Release
3. Now Release tokens can be issued either at a fixed rate or on a bonding curve
4. Once all the milestones have been reached, the feature release is sealed
5. No further tokens may be issued with regards to the release
6. The majority release token holder can now use the release tokens they hold to redeem an NFT corresponding to the release
7. Finally though not necessarily sequentially, the next Feature release schedule is set

### Project Creation
Projects are created through the CLI at least initially, these projects, for the initial purposes will be tied to Git:// repositories, with an access requirement necessary to read repositories. 
```shell=
ships create --project awesome-devtool --repo https://github.com/somedev/awesome-devtool
```

### Feature Release
![feature-release-in-practice](https://user-images.githubusercontent.com/173187/114101465-9e0cc080-987a-11eb-96b7-9b95e31b1bc6.png)


A feature release has a life cycle that corresponds to setting a minting schedule, and naming the feature set. 

The minting schedule helps encourage continous major, minor, and patch releases for a time period that makes sense for the developer. 

Creating incentive for continuous development. In a way because the price of a token falls, there is incentive to earn more tokens to recapture some of the value in the release

### NFT Feature Release 
<img alt="nft-feature-release-practice" src="https://user-images.githubusercontent.com/173187/114103142-710ddd00-987d-11eb-8686-8b34fdcbcf7a.png#center" width=334 height=350/>

Feature Release are sealed then the ability to mint further tokens is frozen and the majority token holder has the ability to redeem a NFT that corresponds to "owning" the release. 

This redemption process can be done through a weighted random holding process if not by absolute majority holding.

## SHPS Token
SHPS is a governance and protocol token that allows SHPS holders to stake SHPS and earn protocol fee rewards charged for Release Token transactions.

This allows SHPS holder to retrieve a periodic fee payout for corresponding to all of the releases in the network. 

To incentivize release producers, release producers are entered into a random weighted selection process to issue a small portion of SHPS Tokens to producers so they can benefit from the Network they are helping to popularlize. This selection process will initially be a trusted process, and then move to a decentralized process, as things develop. 

Periodically additional SHPS Tokens will be issued to staking SHPS holders as well, to incentivize SHPS Token holders to continue holding, vs short term speculating. 

SHPS holders are also able to make protocol governance suggestions, by staking, and these governance suggestions, and changes will be held periodically based on a schedule. 

The initial roll out for these features will be very manual in the beginning as the structure and shape that the protocol desires unfolds. Prior to launch we will set a schedule in which governance changes will be made, initially quite frequently, then decreasing in frequency as the network stabilizes.

## Network Effects and Dynamics

Building a network is really contingent on growing the community of release producers and consumers.

Open source code is social, release producers are encouraged to create an allocation for contributors that can be claimed via email. 

This makes it easy for non SHIPS participants to automatically become participants. 

Additionally with added features for offering premium support. This allows open source developers to access a broader consumer base via free additional knowledge base and support ticket software.

Finally with the growing amount of producers, and the issuing of SHPS to producers and investors we are able to build towards decentralization with a diverse set of protocol holders that can then make support suggestions.

### Initial Support Set
It is trivial to support all languages and ecosystems with this codebase. The initial set of supported languages will be Typescript/Javascript and Rust.

However, there is value in creating specific support for specific languages in a reliable fashion. 

This limitation will allow the ecosystem to move beyond supporting code, and move into also supporting digital assets more broadly. 

For that the structure must be in place to reliably make the release data captured usable by the ecosystems they support.

### Data Storage
There is a strong need to store the releases themselves, and metadata about the release in a structured format.

The initial data format will conform to an IPLD compatible format using content ids as used in the ipfs ecosystem, but across systems. 

See the recent codebase shift in IPLD to allow IPLD compatible data to be more readily stored in different storage systems. 

We aim to make this possible with our system as well to flexible be able to store data in the decentralized fashion that suits our need at any point in time without lock in.

