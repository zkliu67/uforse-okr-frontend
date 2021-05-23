# LOGIN
/login: {
  req: {
    username: "",
    password: ""
  },
  res: {
    success: true,
    result: {
      id: '',
      username: '',  
    }
  }
}

# REGISTER
/register: {
  req: {
    username: "",
    password: "",
    password2: "",
  },
  res: {
    success: true,
    result: {
      id: '',
      username: '',  
    }
  }
}

# LOGOUT
/logout: {
  req: {
    id: "",
  },
  res: {
    success: true
  }
}

# Get All Okrs
/allOkrs: {
  res: {
    success: true,
    result: [
      {
        okr
      }
    ]
  }
}

# Get All Okrs by employerId
/allOkrs?employer={employerId}: {
  res: {
    success: true,
    result: [
      ...,
      {
        "id": "npxl5AtBJpOhGxooSW9P",
        "target": "提高页面响应速度和用户体验",
        "department": "",
        "startDate": "2021.01.30",
        "endDate": "2021.04.30",
        "Assignee": "Sherry",
        "score": "80",
        "krs": [
          {
            "id": "soKW1ufy38KahykGstOh",
            "kr": "提高页面访问效率，访问速度达到100ms以内",
            "weight": "80"
          }
        ]
      }
    ]
  }
}

# POST: Create new okr
/okr?employer={employerId}: {
  req: {
    okr: {
      "target": "提高页面响应速度和用户体验",
      "department": "",
      "startDate": "2021.01.30",
      "endDate": "2021.04.30",
      "Assignee": "Sherry",
      "krs": [
        {
          "id": "soKW1ufy38KahykGstOh",
          "kr": "提高页面访问效率，访问速度达到100ms以内",
          "weight": "80"
        }
      ]
    }
  },
  res: {
    success: true
  }
}

# Modify okr item
/okr?employer={employerId}?okr={okrId}: {
  req: {
    okr: {
      {
        "id": "npxl5AtBJpOhGxooSW9P",
        "target": "提高页面响应速度和用户体验",
        "department": "",
        "startDate": "2021.01.30",
        "endDate": "2021.04.30",
        "Assignee": "Sherry",
        "score": "80",
        "krs": [
          {
            "id": "soKW1ufy38KahykGstOh",
            "kr": "提高页面访问效率，访问速度达到100ms以内",
            "weight": "80"
          }
        ]
      }
    }
  },
  req: {
    success: true
  }
}