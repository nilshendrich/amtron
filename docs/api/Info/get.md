# Other Information

This section includes several commands to get additional information. Instead of using the parameter "DevKey" "Pin" is used. Nevertheless the number to be given is the same.

## Get QSInfo

* **URL**

  /QSInfo?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
  * **Code:** 200
  
    **Datatypes:**

    **Content:**

    ```js
    {
      "HMHW":[string],
      "HMSW":[string],
      "HMTP":[string],
      "HMIO":[string],
      "HMTI":[number],
      "HMTE":[number],
      "HMES":[string],
      "RFVS":null,
      "WFVS":[string],   /* WiFi Firmware Version */
      "HCHW":[string],
      "HCSW":[string],
      "HCIO":[string],
      "HCCP":[string],
      "HCES":[number],
      "AMOM":[string],   /* Current Mode */
      "AMST":[string],   /* Current State */
      "AMCT":[string],
      "AMPH":[number],
      "AMFC":[number],
      "AMSN":[number],
      "AMIN":[string],
      "AMES":[boolean],
      "AMFI":[boolean],
      "AMPS":[boolean],
      "HCMC":[string],
      "HCME":[number]
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/QSInfo?Pin=[devkey]'
  ```

## Get VehicleInfo

* **URL**

  /VehicleInfo?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
  * **Code:** 200

    **Datatypes:**

    **Content:**

    ```js
    {
      "EVPhase":[string],
      "EVMinCur":[string],
      "EVMaxCur":[string],
      "EVPrio"::[boolean]
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/VehicleInfo?Pin=[devkey]'
  ```

## Get TimeInfo

* **URL**

  /TimeInfo?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
  * **Code:** 200

    **Datatypes:**

    **Content:**

    ```js
    {
      "LocTime":[number],
      "Summer"::[boolean],
      "Tz":[number]   /* Timezone offset in minutes */
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/TimeInfo?Pin=[devkey]'
  ```

## Get CustomerInfo

* **URL**

  /CustomerInfo?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
  * **Code:** 200

    **Datatypes:**

    **Content:**

    ```js
    {
      "AMCC":[number],
      "Auth"::[boolean],
      "DevName":[string],  /* Wallbox Name */
      "AutoChg":[boolean],
      "ChgContinue":[boolean],
      "STOP":[boolean],
      "Color":[number],
      "BEEP":[boolean],
      "WLAN":[boolean]
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/CustomerInfo?Pin=[devkey]'
  ```

## Get InstallInfo

* **URL**

  /InstallInfo?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
  * **Code:** 200

    **Datatypes:**

    **Content:**

    ```js
    {
      "AMIC":[number],
      "AMHM":[boolean],
      "AMSE":[boolean],
      "ISEN":[boolean],
      "MROP":[boolean]
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/InstallInfo?Pin=[devkey]'
  ```

## Get SupportInfo

* **URL**

  /SupportInfo?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
    **Code:** 200

    **Datatypes:**

    **Content:**

    ```js
    {
      "SerialNumber":[number],
      "OrderNumber":[string],
      "Hcc3HwVersion":[string],
      "Hcc3SwVersion":[string],
      "BuildNumber":[string],
      "Hcc3ErrorCode":[number],
      "HmiHwVersion":[string],
      "HmiSwVersion":[string],
      "HmiErrorState":[string],
      "WlanFwVersion":[string],  /* WiFi Firmware Version */
      "Multi":[string]
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/SupportInfo?Pin=[devkey]'
  ```

## Get EnergyManagement

* **URL**

  /EnergyManagement?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
  * **Code:** 200

    **Datatypes:**

    **Content:**

    ```js
    {
      "EnergyManagerType":[string],
      "EnergyManagerIpAddress":[string]
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/EnergyManagement?Pin=[devkey]'
  ```

## Get LanStatus

* **URL**

  /LanStatus?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
  * **Code:** 200

    **Datatypes:**

    **Content:**

    ```js
    {
      "IpAddress":[string],
      "Netmask":[string],
      "GatewayIp":[string],
      "AddressSource":[string],
      "Hostname":[string],
      "MacAddress":[string]
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/LanStatus?Pin=[devkey]'
  ```

## Get LanSettings

* **URL**

  /LanSettings?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
  * **Code:** 200

    **Datatypes:**

    **Content:**

    ```js
    {
      "UseStaticAddresses":[boolean],  /* use static IP if true; DHCP if false */
      "IpAddress":[string],  /* static IP Address used if UseStaticAddresses is true */
      "Netmask":[string],   /* netmask used in UseStaticAddresses if true */
      "GatewayIp":[string]   /* Gateway IP used if UseStaticAddresses is true */
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/LanSettings?Pin=[devkey]'
  ```

## Get WlanStatus

* **URL**

  /WlanStatus?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
  * **Code:** 200
  
    **Datatypes:**

    **Content:**

    ```js
    {
      "ApConnStatus":[string],
      "ApMacStatus":[string],
      "ApSsidStatus":[string],
      "ApChannelStatus":[number],
      "ApBssidStatus":[string],
      "StaConnStatus":[string],
      "StaMacStatus":[string],
      "StaChannelStatus":[number],
      "StaBssidStatus":[string],
      "ApIpStatus":[string],
      "ApGatewayStatus":[string],
      "ApSubnetStatus":[string],
      "ApIpSourceStatus":[string],
      "StaLocalMacStatus":[string],
      "StaIpStatus":[string],
      "StaGatewayStatus":[string],
      "StaSubnetStatus":[string],
      "StaIpSourceStatus":[string],
      "Rssi":-38,
      "Clients":[number]
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/WlanStatus?Pin=[devkey]'
  ```

## Get WlanApSettings

* **URL**

  /WlanApSettings?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
  * **Code:** 200

    **Datatypes:**

    **Content:**

    ```js
    {
      "ApSSID":[string],
      "ApChannel":[number],
      "ApSecurityMode":[string],
      "ApCountryCode":[string]
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/WlanApSettings?Pin=[devkey]'
  ```

## Get WlanStaSettings

* **URL**

  /WlanStaSettings?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
  * **Code:** 200

    **Datatypes:**

    **Content:**

    ```js
    {
      "SSID":[string],
      "BSSID":[string],
      "SecurityMode":[string],
      "UseStaticAddresses"::[boolean],
      "StaticIpAddress":[string],
      "StaticNetmask":[string],
      "StaticGatewayIpAddress":[string]
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/WlanStaSettings?Pin=[devkey]'
  ```

## Get RfID

* **URL**

  /RfID?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
  * **Code:** 200

    **Datatypes:**

    **Content:**

    ```js
    {
      "EM4102":[boolean],
      "HITAG1S":[boolean],
      "HITAG2":[boolean],
      "EM4150":[boolean],
      "ISOFDX":[boolean],
      "AWID":[boolean],
      "PYRAMID":[boolean],
      "KERI":[boolean],
      "ISO14443A":[boolean],
      "ISO14443B":[boolean],
      "ISO15693":[boolean],
      "LEGIC":[boolean],
      "HIDICLASS":[boolean],
      "FELICA":[boolean]
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/RfID?Pin=[devkey]'
  ```

## Get ExtensionsInfo

* **URL**

  /ExtensionsInfo?Pin=:devKey

* **Method:**
  
  `GET`
  
* **URL Params**

   **Required:**

   `Pin=[integer]`

* **Success Response:**
  
  * **Code:** 200

    **Datatypes:**

    **Content:**

    ```js
    {
      "MSEN"::[boolean]
    }
    ```

* **Error Response:**

  * **Code:** 403 FORBIDDEN

* **CURL Example**

  ```bash
  curl -H 'Accept: application/json' 'http://[amtron]:25000/MHCP/1.1/ExtensionsInfo?Pin=[devkey]'
  ```
