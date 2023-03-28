**Tariff parameters**
----

Set Tariff data in order to control time based charging, i.e. 'DevMode' equals 'Time'.

* **URL**

  /TariffData?DevKey=:devKey

* **Method:**
  
  `POST`
  
*  **URL Params**

   **Required:**
 
   `devKey=[integer]`

* **Data Params** <br />
    
  ```
  {
  	"Permanent": [boolean],           /* if changes made here are saved permanently */
    "MaxCurrT1": [number],           /* current per phase in A while charging with Time control during main tariff */
    "BeginH_T1": [number],           /* Hour component of start of the main tariff time window */
    "BeginM_T1": [number],           /* Minute component of start of the main tariff time window */
    "PriceT1": [number],           /* price during main tariff in tenths of a cent*/
    "MaxCurrT2": [number],           /* current per phase in A while charging with Time control during secondary tariff */
    "BeginH_T2": [number],           /* Hour component of start of the secondary tariff time window */
    "BeginM_T2": [number],           /* Minute component of start of the secondary tariff time window */
    "PriceT2": [number]           /* price during secondary tariff in tenths of a cent*/
  }
  ```

* **Success Response:**
  
  * **Code:** 200
 
* **Error Response:**

  * **Code:** 401 UNAUTHORIZED

  OR

  * **Code:** 400 BAD REQUEST

* **Sample Data Params:**

  ```json
  {
  	"Permanent": true,
    "MaxCurrT1": 0, 
    "BeginH_T1": 6,
    "BeginM_T1": 0,
    "PriceT1": 510,
    "MaxCurrT2": 16,
    "BeginH_T2": 0,
    "BeginM_T2": 0,
    "PriceT2": 60
  }
  ```

* **CURL Example**
```bash
curl -X POST -d '{"Permanent": true, "MaxCurrT1": 0, "BeginH_T1": 6, "BeginM_T1": 0, "PriceT1": 510, "MaxCurrT2": 16, "BeginH_T2": 0, "BeginM_T2": 0, "PriceT2": 60 }' -H 'Content-Type: application/json' -v 'http://[amtron]:25000/MHCP/1.0/TariffData?DevKey=[devkey]'
```

