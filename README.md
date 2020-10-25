# Sitelink Manager API

The sitelink manager API is responsible for retrieving promotions, units, and unit types from Sitelink directly via their API. 


## Hosting
---
_SECTION OMITTED FOR SECURITY PURPOSES_

## Requirements
---
This project is configured to use docker for local testing, here's what you need to get started:

### Dependencies

- [Docker](https://www.docker.com/)

### Getting started

1. Build the project
`docker-compose build`

3. Use docker-compose to run the API
`docker-compose up`

`Note: Locally nodemon is used for auto-restart of application while coding, so no need to kill / restart everytime there's a code change`

## Secrets
_SECTION OMITTED FOR SECURITY PURPOSES_

## State
---

### Active Locations  

`Eagle Guard`  
- eg-l001  
- eg-l002  
- eg-l003  
- eg-l004  
- eg-l005  
- eg-l006  

### Promotional Message Rules

* iTotalUnits < 2 OR occupied percent >= 0.9 : "Call for Availability"

* occupied percent >= 0.8 AND occupied percent < 0.9 : "50% off first month"

* occupied percent >= 0.7 AND occupied percent < 0.8 : "First month free"

* occupied percent < 0.7 : "50% off first 3 months"

### Sizes

* SMALL - `5x10`

* MEDIUM - `7x12; 10x10; 10x15`

* LARGE - `10x20 OR ANYTHING LARGER`

* PARKING - `sTypeName is "Parking"`

### Flash Sale Locations

There are currently no `Flash Sale` locations set

### Rate Discounts

* `dcPushRate - no change`
* `dcStdRate - dcStdRate + 20%`

### Sitelink Messages
```
{
        "$attributes": {
            "id": "Table1",
            "rowOrder": "0"
        },
        "SiteID": "33091",
        "iCurrencyDecimals": "2",
        "iTaxDecimals": "2",
        "dcTax1Rate_Rent": "0.0000",
        "dcTax2Rate_Rent": "0.0000",
        "iRegionalOptions": "0",
        "UnitTypeID": "277",
        "sTypeName": "Drive-Up",
        "bChargeTax1": "true",
        "bChargeTax2": "true",
        "iDefLeaseNum": "1",
        "bMobile": "false",
        "bClimate": "false",
        "bPower": "false",
        "bAlarm": "false",
        "bInside": "false",
        "iFloor": "1",
        "dcWidth": "10.0000",
        "dcLength": "20.0000",
        "dcArea": "200.0000",
        "dcPushRate_NotRounded": "117.6500",
        "dcPushRate": "117.6500",
        "dcStdRate": "95",
        "dcStdWeeklyRate": "0.0000",
        "iTotalUnits": "19",
        "iTotalOccupied": "19",
        "iTotalVacant": "0",
        "iTotalReserved": "0",
        "UnitID_FirstAvailable": "15945",
        "sUnitName_FirstAvailable": "101",
        "UnitID_Representative": "15945",
        "sUnitName_Representative": "101",
        "dcAdminFee": "25.0000",
        "dcReservationFee": "25.0000",
        "bRented_FirstAvailable": "true",
        "bExcludeFromInsurance": "false",
        "ConcessionID": "1542",
        "DefaultCoverageID": "-999",
        "dcWebRate": "117.6500",
        "dcBoardRate": "117.6500",
        "dcPreferredRate": "117.6500",
        "iPreferredChannelType": "0",
        "bPreferredIsPushRate": "false",
        "bLeaseIsESignEnabled": "false",
        "PromoMessage": "Call for availability"
    }
```
