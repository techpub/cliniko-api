Patients
============
> Patients are the people that book in for appointments.  There isn't much in Cliniko that doesn't revolve around patients.
>
> When you're working with patient information, make sure you abide by the relevant regulations for security and privacy.

* [Get Patients](#get-patients "This will return all patients.")
* [Get Deleted Patients](#get-deleted-patients "This will return all deleted patients.")
* [Get Archived Patients](#get-archived-patients "This will return all archived patients.")
* [Get Patient](#get-patient "This will return a specified patient.")
* [Create Patient](#create-patient "This will create a patient.")
* [Update Patient](#update-patient "This will update a patient.")
* [Delete Patient](#delete-patient "This will delete a patient.")

Get Patients
----------------

**Resources**
* ```GET /patients``` get all patients


**Example Request**
```shell
curl https://api.cliniko.com/v1/patients \
  -u API_KEY: \
  -H 'Accept: application/json' \
  -H 'User-Agent: APP_VENDOR_NAME (APP_VENDOR_EMAIL)'
```

**Example Response**
```json
{
  "patients": [
    {
      "address_1": "1 Smith Street",
      "address_2": "",
      "address_3": "",
      "archived_at": "",
      "city": "Melbourne",
      "country": "Australia",
      "created_at": "2013-03-26T14:00:00Z",
      "date_of_birth": "2001-05-26",
      "deleted_at": "",
      "email": "peter@example.com",
      "emergency_contact": "",
      "first_name": "Peter",
      "invoice_default_to": "Super Insurance",
      "invoice_email": "super.insurance@example.com",
      "invoice_extra_information": "Insurance #123456\r\nClaim #123456",
      "gender": "Male",
      "id": 1,
      "last_name": "Patientman",
      "notes": "",
      "occupation": "",
      "old_reference_id": "",
      "post_code": "3000",
      "referral_source": "",
      "reminder_type": "SMS & Email",
      "state": "Victoria",
      "title": "Mr",
      "updated_at": "2013-03-26T14:00:00Z",
      "concession_type": {
        "links": {
          "self": "https://api.cliniko.com/v1/concession_types/123"
        }
      },
      "patient_phone_numbers": [
        {
          "phone_type": "Mobile",
          "number": "61444444444"
        },
        {
          "phone_type": "Home",
          "number": "61399999999"
        }
      ],
      "medical_alerts": {
        "links": {"self": "https://api.cliniko.com/v1/patients/1/medical_alerts?page=1"}
      },
      "invoices": {
        "links": {
          "self": "https://api.cliniko.com/v1/patients/1/invoices?page=1"
        }
      },
      "appointments": {
        "links": {
          "self": "https://api.cliniko.com/v1/patients/1/appointments?page=1"
        }
      },
      "links": {"self": "https://api.cliniko.com/v1/patients/1"}
    }
  ],
  "total_entires": 1,
  "links": {"self": "https://api.cliniko.com/v1/patients?page=1"}
}
```

Get Deleted Patients
----------------

**Resources**
* ```GET /patients/deleted``` get all deleted patients

**Example Request**
```shell
curl https://api.cliniko.com/v1/patients/deleted \
  -u API_KEY: \
  -H 'Accept: application/json' \
  -H 'User-Agent: APP_VENDOR_NAME (APP_VENDOR_EMAIL)'
```

**Example Response**
```json
{
  "patients": [
    {
      "address_1": "1 Smith Street",
      "address_2": "",
      "address_3": "",
      "archived_at": "2013-06-05T14:37:18Z",
      "city": "Melbourne",
      "country": "Australia",
      "created_at": "2013-03-26T14:00:00Z",
      "date_of_birth": "2001-05-26",
      "deleted_at": "2013-06-05T14:38:48Z",
      "email": "peter@example.com",
      "emergency_contact": "",
      "first_name": "Peter",
      "invoice_default_to": "Super Insurance",
      "invoice_email": "super.insurance@example.com",
      "invoice_extra_information": "Insurance #123456\r\nClaim #123456",
      "gender": "Male",
      "id": 1,
      "last_name": "Patientman",
      "notes": "",
      "occupation": "",
      "old_reference_id": "",
      "post_code": "3000",
      "referral_source": "",
      "reminder_type": "Email",
      "state": "Victoria",
      "title": "Mr",
      "updated_at": "2013-03-26T14:00:00Z",
      "concession_type": {
        "links": {
          "self": "https://api.cliniko.com/v1/concession_types/123"
        }
      },
      "patient_phone_numbers": [
        {
          "phone_type": "Mobile",
          "number": "61444444444"
        },
        {
          "phone_type": "Home",
          "number": "61399999999"
        }
      ],
      "medical_alerts": {
        "links": {"self": "https://api.cliniko.com/v1/patients/1/medical_alerts?page=1"}
      },
      "invoices": {
        "links": {
          "self": "https://api.cliniko.com/v1/patients/1/invoices?page=1"
        }
      },
      "appointments": {
        "links": {
          "self": "https://api.cliniko.com/v1/patients/1/appointments?page=1"
        }
      },
      "links": {"self": "https://api.cliniko.com/v1/patients/1"}
    }
  ],
  "total_entires": 1,
  "links": {"self": "https://api.cliniko.com/v1/patients/deleted?page=1"}
}
```

Get Archived Patients
----------------

**Resources**
* ```GET /patients/archived``` get all archived patients

**Example Request**
```shell
curl https://api.cliniko.com/v1/patients/archived \
  -u API_KEY: \
  -H 'Accept: application/json' \
  -H 'User-Agent: APP_VENDOR_NAME (APP_VENDOR_EMAIL)'
```

**Example Response**
```json
{
  "patients": [
    {
      "address_1": "1 Smith Street",
      "address_2": "",
      "address_3": "",
      "archived_at": "2013-06-05T14:37:18Z",
      "city": "Melbourne",
      "country": "Australia",
      "created_at": "2013-03-26T14:00:00Z",
      "date_of_birth": "2001-05-26",
      "deleted_at": "",
      "email": "peter@example.com",
      "emergency_contact": "",
      "first_name": "Peter",
      "invoice_default_to": "Super Insurance",
      "invoice_email": "super.insurance@example.com",
      "invoice_extra_information": "Insurance #123456\r\nClaim #123456",
      "gender": "Male",
      "id": 1,
      "last_name": "Patientman",
      "notes": "",
      "occupation": "",
      "old_reference_id": "",
      "post_code": "3000",
      "referral_source": "",
      "reminder_type": "SMS",
      "state": "Victoria",
      "title": "Mr",
      "updated_at": "2013-03-26T14:00:00Z",
      "concession_type": {
        "links": {
          "self": "https://api.cliniko.com/v1/concession_types/123"
        }
      },
      "patient_phone_numbers": [
        {
          "phone_type": "Mobile",
          "number": "61444444444"
        },
        {
          "phone_type": "Home",
          "number": "61399999999"
        }
      ],
      "medical_alerts": {
        "links": {"self": "https://api.cliniko.com/v1/patients/1/medical_alerts?page=1"}
      },
      "invoices": {
        "links": {
          "self": "https://api.cliniko.com/v1/patients/1/invoices?page=1"
        }
      },
      "appointments": {
        "links": {
          "self": "https://api.cliniko.com/v1/patients/1/appointments?page=1"
        }
      },
      "links": {"self": "https://api.cliniko.com/v1/patients/1"}
    }
  ],
  "total_entires": 1,
  "links": {"self": "https://api.cliniko.com/v1/patients/archived?page=1"}
}
```

Get Patient
------------

**Resources**
* ```GET /patients/:id``` get a specified patient

**Example Request**
```shell
curl https://api.cliniko.com/v1/patients/1 \
  -u API_KEY: \
  -H 'Accept: application/json' \
  -H 'User-Agent: APP_VENDOR_NAME (APP_VENDOR_EMAIL)'
```

**Example Response**
```json
{
  "address_1": "1 Smith Street",
  "address_2": "",
  "address_3": "",
  "archived_at": "",
  "city": "Melbourne",
  "country": "Australia",
  "created_at": "2013-03-26T14:00:00Z",
  "date_of_birth": "2001-05-26",
  "deleted_at": "",
  "email": "peter@example.com",
  "emergency_contact": "",
  "first_name": "Peter",
  "invoice_default_to": "Super Insurance",
  "invoice_email": "super.insurance@example.com",
  "invoice_extra_information": "Insurance #123456\r\nClaim #123456",
  "gender": "Male",
  "id": 1,
  "last_name": "Patientman",
  "notes": "",
  "occupation": "",
  "old_reference_id": "",
  "post_code": "3000",
  "referral_source": "",
  "reminder_type": "None",
  "state": "Victoria",
  "title": "Mr",
  "updated_at": "2013-03-26T14:00:00Z",
  "concession_type": {
    "links": {
      "self": "https://api.cliniko.com/v1/concession_types/123"
    }
  },
  "patient_phone_numbers": [
    {
      "phone_type": "Mobile",
      "number": "61444444444"
    },
    {
      "phone_type": "Home",
      "number": "61399999999"
    }
  ],
  "medical_alerts": {
    "links": {"self": "https://api.cliniko.com/v1/patients/1/medical_alerts?page=1"}
  },
  "invoices": {
    "links": {
      "self": "https://api.cliniko.com/v1/patients/1/invoices?page=1"
    }
  },
  "appointments": {
    "links": {
      "self": "https://api.cliniko.com/v1/patients/1/appointments?page=1"
    }
  },
  "links": {"self": "https://api.cliniko.com/v1/patients/1"}
}
```

Create Patient
----------------
**Resources**
* ```POST /patients``` create a patient

**Example Request**
```shell
curl https://api.cliniko.com/v1/patients \
  -u API_KEY: \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'User-Agent: APP_VENDOR_NAME (APP_VENDOR_EMAIL)' \
  -d '{ "first_name": "John", "last_name": "Snow" }' \
  -X POST
```
**Example Response**
```
Headers { Location: http://api.cliniko.com/patients/1 }
```
```json
{
  "address_1": "1 Smith Street",
  "address_2": "",
  "address_3": "",
  "archived_at": "",
  "city": "",
  "country": "",
  "created_at": "2013-03-26T14:00:00Z",
  "date_of_birth": "",
  "deleted_at": "",
  "email": "",
  "emergency_contact": "",
  "first_name": "John",
  "invoice_default_to": "",
  "invoice_email": "",
  "invoice_extra_information": "",
  "gender": "",
  "id": 1,
  "last_name": "Snow",
  "notes": "",
  "occupation": "",
  "old_reference_id": "",
  "post_code": "",
  "referral_source": "",
  "reminder_type": "SMS & Email",
  "state": "",
  "title": "",
  "updated_at": "2013-03-26T14:00:00Z",
  "patient_phone_numbers": [],
  "medical_alerts": {
    "links": {"self": "https://api.cliniko.com/v1/patients/1/medical_alerts?page=1"}
  },
  "invoices": {
    "links": {
      "self": "https://api.cliniko.com/v1/patients/1/invoices?page=1"
    }
  },
  "appointments": {
    "links": {
      "self": "https://api.cliniko.com/v1/patients/1/appointments?page=1"
    }
  },
  "links": {"self": "https://api.cliniko.com/v1/patients/1"}
}
```

Update Patient
----------------
**Resources**
* ```PUT /patients/:id``` update a patient

**Example Request**
```shell
curl https://api.cliniko.com/v1/patients/1 \
  -u API_KEY: \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -H 'User-Agent: APP_VENDOR_NAME (APP_VENDOR_EMAIL)' \
  -d '{ "first_name": "John", "last_name": "Snow" }' \
  -X PUT
```
**Example Response**
```json
{
  "address_1": "1 Smith Street",
  "address_2": "",
  "address_3": "",
  "archived_at": "",
  "city": "Melbourne",
  "country": "Australia",
  "created_at": "2013-03-26T14:00:00Z",
  "date_of_birth": "2001-05-26",
  "deleted_at": "",
  "email": "peter@example.com",
  "emergency_contact": "",
  "first_name": "John",
  "invoice_default_to": "Super Insurance",
  "invoice_email": "super.insurance@example.com",
  "invoice_extra_information": "Insurance #123456\r\nClaim #123456",
  "gender": "Male",
  "id": 1,
  "last_name": "Snow",
  "notes": "",
  "occupation": "",
  "old_reference_id": "",
  "post_code": "3000",
  "referral_source": "",
  "reminder_type": "SMS & Email",
  "state": "Victoria",
  "title": "Mr",
  "updated_at": "2013-03-26T14:00:00Z",
  "patient_phone_numbers": [
    {
      "phone_type": "Mobile",
      "number": "61444444444"
    },
    {
      "phone_type": "Home",
      "number": "61399999999"
    }
  ],
  "medical_alerts": {
    "links": {"self": "https://api.cliniko.com/v1/patients/1/medical_alerts?page=1"}
  },
  "invoices": {
    "links": {
      "self": "https://api.cliniko.com/v1/patients/1/invoices?page=1"
    }
  },
  "appointments": {
    "links": {
      "self": "https://api.cliniko.com/v1/patients/1/appointments?page=1"
    }
  },
  "links": {"self": "https://api.cliniko.com/v1/patients/1"}
}
```

Delete Patient
----------------
**Resources**
* ```DELETE /patients/:id``` delete a patient

**Example Request**
```shell
curl https://api.cliniko.com/v1/patients/1 \
  -u API_KEY: \
  -H 'Accept: application/json' \
  -H 'User-Agent: APP_VENDOR_NAME (APP_VENDOR_EMAIL)' \
  -X DELETE
```
**Example Response**
A status code of `204 no content` will be returned if successful

Filtering Patients
----------------

For any route that returns a set of patients, you can filter them by:
* ```first_name``` (String)
* ```id``` integer
* ```last_name``` (String)
* ```email``` (String)
* ```old_reference_id``` (String)
* ```updated_at``` DateTime

See [Filtering Results](https://github.com/redguava/cliniko-api#filtering-results) for details on how to apply filters.
