# Rent Phone
## Step - 1 Get the data from intent in Landing or Launcher activity
```
val userIdRentApp:String?=null
   intent?.let {
            if (intent.hasExtra("USER_FROM_RENT")) {
                userIdRentApp = intent.getStringExtra("USER_FROM_RENT")
            }
        }
```
## Step - 2 Call the API to merge the main app user with the rent app user
```
{end point will be main app}/pairUserRentApp
 ```
```
{"deviceType":"Android","userIdRentApp":6618ca07243b27000sdasdf1"","isRent":true,"deviceId":"33C94DA1523FFCDC8562D4CC6E0A1235","userId":"6618ca07243b2700027f4df1"}
```
### Pass value from the intent which we get from rent app into userIdRentApp

```userIdRentApp = userIdRentApp```

```isRent=userIdRentApp!=null```

## Step - 3 Will get the user object in response
```cycleAdsForRentApp```
## Step - 4 Check this flag in API response is true then start the cycle ads without overlay
We need to override the user object with this api response we need to, otherwise we can use the above flag
