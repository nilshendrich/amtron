# Change charge parameters

Control charging of the wallbox.

* **URL**

  /ChargeData?DevKey=:devKey

* **Method:**
  
  `POST`
  
* **URL Params**

   **Required:**

   `devKey=[integer]`

* **Data Params**

  **Datatypes:**
  * `EnumChargeControl: [Continue, Pause, Start, Terminate]`

  All parameters except "Permanent" can be set to null if no change is intended.
  
  ```js
  {
    "Permanent": [boolean],           /* if changes made here are saved permanently */
    "RemoteCurr": [number],           /* current per phase in A while charging with App control */
    "AutoChg": [boolean],             /* true if charging should start automatically */
    "ChgState": [EnumChargeControl],  /* update charge state with value here */
    "Uid": [string]                   /* should always be 00000000 */
  }
  ```

* **Success Response:**
  
  * **Code:** 200

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED

  OR

  * **Code:** 400 BAD REQUEST

* **Sample Data Params:**

  ```js
  {
    "Permanent": true,
    "RemoteCurr": 6,
    "AutoChg": null,
    "ChgState": null,
    "Uid": null
  }
  ```

* **Notes:**

    On (some) chargers that use 3 phases, the remote current can not be smaller than 6A.
  
    It seems like the UID has to be 00000000 for "Start" to work.
