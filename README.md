# sample-publisher-role-app
This app aims to provide sample application that can be used as a developers guide for any app that publisher is creating with intention to publish it on AppShpere.

##  static String login = "/api/auth/login";

  /**
   * The `login` function in TypeScript handles user authentication by verifying credentials, checking
   * OTP verification status, generating access and refresh tokens, and updating user device token.
   * @param req - The `login` function you provided is an asynchronous function that handles user
   * authentication. It takes a `req` parameter, which likely contains information such as the user's
   * email, password, and device token.
   * @returns The `login` function returns an object containing `access_token`, `refresh_token`, and
   * `user` properties.
   */

    "/auth/login": {
      "post": {
        "operationId": "AuthController_login",
        "summary": "login api also used by appSphere",
        "parameters": [],
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/LoginParamsDTO"
              }
            }
          }
        },
        "responses": {
          "201": {
            "description": ""
          }
        },
        "tags": [
          "Auth"
        ]
      }
    },


##  static String socialLogin = "api/auth/social?socialId=";

  /**
   * The function `socialLogin` performs a social login using a Google API endpoint and returns an access
   * token.
   * @param {string} socialId - The `socialId` parameter in the `socialLogin` function is a string that
   * represents the access token used for social login authentication. This access token is passed to the
   * Google API to retrieve user information for authentication and authorization purposes.
   * @returns The `socialLogin` function returns an object containing an `access_token` property.
   */

    "/auth/social": {
      "post": {
        "operationId": "AuthController_googleAuth",
        "summary": "google auth api also used by appSphere",
        "parameters": [
          {
            "name": "socialId",
            "required": true,
            "in": "query",
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "201": {
            "description": ""
          }
        },
        "tags": [
          "Auth"
        ]
      }
    },

##  static String refreshToken = '/api/auth/refresh-token'

  /**
   * The function `refreshAccessToken` takes a refresh token, verifies it, and generates new access and
   * refresh tokens with updated expiration times.
   *
   * :param refreshToken: The `refreshToken` parameter in the `refreshAccessToken` function is a string
   * that represents the refresh token used to generate a new access token and refresh token pair. This
   * function is typically used in authentication systems to refresh the user's access token without
   * requiring the user to log in again. The function dec
   * :type refreshToken: string
   * :return: The `refreshAccessToken` function is returning an object with two properties:
   * `access_token` and `refresh_token`. The `access_token` is generated using the `jwtService.signAsync`
   * method with a payload containing the user's email, userId, and role, and an expiration time of 1
   * day. The `refresh_token` is also generated using the `jwtService.signAsync` method with
   */

    "/auth/refresh-token": {
      "post": {
        "operationId": "AuthController_refreshToken",
        "summary": "refresh token api also used by appSphere",
        "parameters": [],
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/RefreshTokenDTO"
              }
            }
          }
        },
        "responses": {
          "201": {
            "description": ""
          }
        },
        "tags": [
          "Auth"
        ]
      }
    },

##  static String verification = "/api/auth/verify";

  /**
   * The function `resendVerifyOtp` asynchronously sends a verification OTP to the provided email address
   * and returns a success message if successful.
   *
   * :param email: The `email` parameter is a string that represents the email address to which the OTP
   * (One-Time Password) will be sent for verification
   * :type email: string
   * :return: The `resendVerifyOtp` function is returning an object with a message property indicating
   * that the OTP was sent successfully.
   */

    "/auth/verify": {
      "post": {
        "operationId": "AuthController_verify",
        "summary": "otp verify api also used by appSphere",
        "parameters": [],
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/VerifyOtpDTO"
              }
            }
          }
        },
        "responses": {
          "201": {
            "description": ""
          }
        },
        "tags": [
          "Auth"
        ]
      }
    },

##  static String signup = "/api/auth/register";

  /**
   * The function `me` retrieves a user's data with active subscriptions and generates a refresh token
   * for the user.
   * @param {number} userId - The `me` function you provided is an asynchronous function that retrieves a
   * user's information based on the `userId` parameter. It filters the user's active subscriptions,
   * generates a refresh token, and adds it to the user object before returning the user data.
   * @returns The `me` function is returning an object with a `data` property containing the user
   * information fetched from the database. Additionally, a `refresh_token` property is added to the user
   * object before returning it.
   */

    "/auth/register": {
      "post": {
        "operationId": "AuthController_register",
        "summary": "signup api also used by appSphere",
        "parameters": [],
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/CreateUserDTO"
              }
            }
          }
        },
        "responses": {
          "201": {
            "description": ""
          }
        },
        "tags": [
          "Auth"
        ]
      }
    },

##  static String sendOtp = "/api/auth/resend-verify-otp";

  /**
   * The function `resendVerifyOtp` asynchronously sends a verification OTP to the provided email address
   * and returns a success message if successful.
   *
   * :param email: The `email` parameter is a string that represents the email address to which the OTP
   * (One-Time Password) will be sent for verification
   * :type email: string
   * :return: The `resendVerifyOtp` function is returning an object with a message property indicating
   * that the OTP was sent successfully.
   */

    "/auth/resend-verify-otp/{email}": {
      "get": {
        "operationId": "AuthController_resendVerifyOtp",
        "summary": "resend otp verify api also used by appSphere",
        "parameters": [
          {
            "name": "email",
            "required": true,
            "in": "path",
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": ""
          }
        },
        "tags": [
          "Auth"
        ]
      }
    },

##  static String profile = "/api/auth/me";

  /**
   * The function `me` retrieves a user's data with active subscriptions and generates a refresh token
   * for the user.
   * @param {number} userId - The `me` function you provided is an asynchronous function that retrieves a
   * user's information based on the `userId` parameter. It filters the user's active subscriptions,
   * generates a refresh token, and adds it to the user object before returning the user data.
   * @returns The `me` function is returning an object with a `data` property containing the user
   * information fetched from the database. Additionally, a `refresh_token` property is added to the user
   * object before returning it.
   */

    "/auth/me": {
      "get": {
        "operationId": "AuthController_me",
        "summary": "fetch logged in  user credentials api, also used by appSphere",
        "parameters": [],
        "responses": {
          "401": {
            "description": "Unauthorized to access this resource."
          }
        },
        "tags": [
          "Auth"
        ],
        "security": [
          {
            "bearer": []
          }
        ]
      }
    },

##  static String countries = "/api/countries";

/**
 * The function `findAll` asynchronously retrieves a list of countries based on search criteria,
 * pagination, and sorting.
 *
 * :param page: The `page` parameter is used to specify the page number of results to retrieve. It is
 * typically used in pagination to navigate through a large set of data by breaking it into smaller,
 * manageable chunks called pages
 * :param limit: The `limit` parameter specifies the maximum number of records to be returned per page
 * in the pagination. It determines how many items will be displayed on each page of results
 * :param search: The `search` parameter in the `findAll` method is used to filter the results based on
 * the name or country code that partially matches the provided search term. The `where` clause in the
 * query filters the results where either the `name` or `country_code` column contains the search term
 * in (optional)
 * :return: The `findAll` method is returning an object with two properties: `countries` and `total`.
 * The `countries` property contains an array of countries that match the search criteria, and the
 * `total` property contains the total count of countries that match the search criteria.

 */

     "/countries": {
      "get": {
        "operationId": "CountryController_findAll",
        "summary": "fetch countries api also used by appSphere",
        "parameters": [
          {
            "name": "page",
            "required": false,
            "in": "query",
            "schema": {
              "type": "number"
            }
          },
          {
            "name": "limit",
            "required": false,
            "in": "query",
            "schema": {
              "type": "number"
            }
          },
          {
            "name": "search",
            "required": false,
            "in": "query",
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": ""
          }
        },
        "tags": [
          "Countries"
        ]
      }
    },


 
##  static String categories = "/api/category";


  /**
   * This function asynchronously retrieves all categories from a repository and returns them as a
   * Promise.
   * :return: The `getAllCategory` function is returning a Promise that resolves to an array of
   * `Category` objects.
   */

    "/category": {
      "get": {
        "operationId": "CategoryController_getAllCategories",
        "summary": "fetch category api also used by appSphere",
        "parameters": [],
        "responses": {
          "200": {
            "description": ""
          }
        },
        "tags": [
          "category"
        ]
      }
    },
##  static String subscribedApps = '/api/products/subscribed';

/**
 * This TypeScript function retrieves subscribed products for a specific user based on their ID.
 *
 * :param _user: The `_user` parameter is an object representing a user. It seems to have an `id`
 * property that is used to find products related to the user's subscriptions
 * :type _user: any
 * :return: The `getSubscribedProductbyUserId` function returns a Promise with an object containing the
 * following properties:
 * - `status` (string): Indicates the status of the operation, in this case, 'success'.
 * - `data` (optional array of Products): Contains an array of Products related to the user's
 * subscriptions.
 * - `message` (optional string): A message that can be included in the
 */
     "/products/subscribed": {
      "get": {
        "operationId": "ProductsController_getAllSubscribedProducts",
        "summary": "Get all  subscribed products against userId also used by appSphere",
        "parameters": [],
        "responses": {
          "401": {
            "description": "Unauthorized to access this resource."
          }
        },
        "tags": [
          "products"
        ],
        "security": [
          {
            "bearer": []
          }
        ]
      }
    },


##  static String products = "/api/products";

/**
 * This TypeScript function retrieves products based on pagination, category, and search query while
 * filtering user data based on role.
 *
 * :param data: The `getAllProductsPaginated` function takes a `paginationDto` object as a parameter.
 * This object typically contains the following properties:
 * :type data: paginationDto
 * :return: The `getAllProductsPaginated` function returns a Promise that resolves to an object
 * containing two properties: `results` which is an array of Products, and `count` which is a number
 * representing the total count of products.

 */
 "/products": {
      "get": {
        "operationId": "ProductsController_getAllProductsPaginated",
        "summary": "fetch products api also used by appSphere",
        "parameters": [
          {
            "name": "page",
            "required": false,
            "in": "query",
            "schema": {
              "type": "number"
            }
          },
          {
            "name": "pageSize",
            "required": false,
            "in": "query",
            "schema": {
              "type": "number"
            }
          },
          {
            "name": "query",
            "required": false,
            "in": "query",
            "schema": {
              "type": "string"
            }
          },
          {
            "name": "categoryId",
            "required": false,
            "in": "query",
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": ""
          }
        },
        "tags": [
          "products"
        ]
      },

    },


##  static String productsByStatus = "/api/products/status";

/**
 * The function `getAllPublishedProductsPaginated` retrieves published products based on pagination,
 * search query, and category ID, returning results with average ratings.
 *
 * :param data: The `getAllPublishedProductsPaginated` function takes a `paginationDto2` object as its
 * parameter, which includes the following properties:
 * :type data: paginationDto2
 * :return: The `getAllPublishedProductsPaginated` function returns a Promise that resolves to an
 * object containing two properties: `results` and `count`. The `results` property is an array of
 * `Products` and the `count` property is a number representing the total count of products.
 */

    "/products/status": {
      "get": {
        "operationId": "ProductsController_getAllPublishedProductsPaginated",
        "summary": "fetch published products api also used by appSphere",
        "parameters": [
          {
            "name": "page",
            "required": false,
            "in": "query",
            "schema": {
              "type": "number"
            }
          },
          {
            "name": "pageSize",
            "required": false,
            "in": "query",
            "schema": {
              "type": "number"
            }
          },
          {
            "name": "query",
            "required": false,
            "in": "query",
            "schema": {
              "type": "string"
            }
          },
          {
            "name": "status",
            "required": false,
            "in": "query",
            "schema": {
              "type": "string"
            }
          },
          {
            "name": "categoryId",
            "required": false,
            "in": "query",
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "401": {
            "description": "Unauthorized to access this resource."
          }
        },
        "tags": [
          "products"
        ],
        "security": [
          {
            "bearer": []
          }
        ]
      }
    },


##  static String postRating = "/api/rating/create";

/**
 * The function `addRating` in TypeScript adds a new rating and comment for a product, calculates the
 * average rating for the product, and updates the cumulative rating for the product.
 *
 * :param data: AddRatingDTO object containing rating, comment, and appIdentifier
 * :type data: AddRatingDTO
 * :param userId: The `userId` parameter in the `addRating` function represents the unique identifier
 * of the user who is adding the rating for a product. This parameter is used to associate the rating
 * with the specific user who provided it
 * :type userId: number
 * :return: The `savedRating` object is being returned from the `addRating` function.
 */

    "/rating/create": {
      "post": {
        "operationId": "RatingController_createRating",
        "summary": "rating post api also used by appSphere",
        "parameters": [],
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/AddRatingDTO"
              }
            }
          }
        },
        "responses": {
          "401": {
            "description": "Unauthorized to access this resource."
          }
        },
        "tags": [
          "rating"
        ],
        "security": [
          {
            "bearer": []
          }
        ]
      }
    },


##  static String getRating = "/api/rating/paginatedRatings";

/**
 * The function `getPaginatedRatings` retrieves paginated ratings based on page number, page size, and
 * optional app identifier, including counts of ratings for each value and average rating.
 *
 * :param getPaginatedRatings: The `getPaginatedRatings` function takes an object as a parameter with
 * the following properties:
 * :type getPaginatedRatings: getPaginatedRatings
 * :return: The `getPaginatedRatings` function returns different data based on the conditions:
 */

    "/rating/paginatedRatings": {
      "get": {
        "operationId": "RatingController_getPaginatedRatings",
        "summary": "fetch rating  also used by appSphere",
        "parameters": [
          {
            "name": "page",
            "required": false,
            "in": "query",
            "schema": {
              "type": "number"
            }
          },
          {
            "name": "pageSize",
            "required": false,
            "in": "query",
            "schema": {
              "type": "number"
            }
          },
          {
            "name": "appIdentifier",
            "required": false,
            "in": "query",
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "401": {
            "description": "Unauthorized to access this resource."
          }
        },
        "tags": [
          "rating"
        ],
        "security": [
          {
            "bearer": []
          }
        ]
      }
    },

##  static String getUserRating = "/api/rating/";

/**
 * The function `getProductRatingsByAppId` retrieves product ratings based on the app identifier and
 * user ID.
 *
 * :param appIdentifier: The `appIdentifier` parameter is a string that represents the identifier of a
 * specific application. It is used to filter and retrieve product ratings associated with that
 * particular application
 * :type appIdentifier: string
 * :param userId: The `userId` parameter is the unique identifier of the user for whom you want to
 * retrieve product ratings
 * :type userId: number
 * :return: The `getProductRatingsByAppId` function returns an object with a status code of 200, a
 * success message, and the data containing ratings for a specific product identified by
 * `appIdentifier` and a specific user identified by `userId`. The ratings include the rating value,
 * comment, product details (id and title), and user details (id and avatar).

 */

 "/rating/{appIdentifier}": {
  "get": {
    "operationId": "RatingController_getRatings",
    "summary": "All ratings against appIdentifier and logged-in user, also used by AppSphere.",
    "parameters": [
      {
        "name": "appIdentifier",
        "required": true,
        "in": "path",
        "schema": {
          "type": "string"
        }
      }
    ],
    "responses": {
      "401": {
        "description": "Unauthorized to access this resource."
      }
    },
    "tags": ["rating"],
    "security": [
      {
        "bearer": []
      }
    ]
  }
}

  
## from here
