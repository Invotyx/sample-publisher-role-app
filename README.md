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

##  static String socialLogin = "api/auth/social?socialId=";

  /**
   * The function `socialLogin` performs a social login using a Google API endpoint and returns an access
   * token.
   * @param {string} socialId - The `socialId` parameter in the `socialLogin` function is a string that
   * represents the access token used for social login authentication. This access token is passed to the
   * Google API to retrieve user information for authentication and authorization purposes.
   * @returns The `socialLogin` function returns an object containing an `access_token` property.
   */

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


##  static String categories = "/api/category";

  /**
   * This function asynchronously retrieves all categories from a repository and returns them as a
   * Promise.
   * :return: The `getAllCategory` function is returning a Promise that resolves to an array of
   * `Category` objects.
   */

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


##  static String subscription = "/api/subscription";

/**
 * The `findAll` function retrieves subscriptions associated with a specific user, including related
 * package and product information.
 *
 * :param user: The `findAll` method is an asynchronous function that retrieves subscriptions
 * associated with a specific user. The `user` parameter represents the user for whom the subscriptions
 * are being fetched. The method uses the `subscriptionRepo` repository to find subscriptions based on
 * the user's ID. It includes various relations such as package
 * :return: The `findAll` method is returning an object with a `data` property containing the
 * subscriptions found for the specified user.
 */


##  static String restoreSubscription = "/api/subscription/restore";

/**
 * The function `restoreSubscription` retrieves an active subscription for a specific user and app
 * identifier.
 *
 * :param appIdentifier: The `appIdentifier` parameter in the `restoreSubscription` function is a
 * string that represents the identifier of the application for which the subscription needs to be
 * restored. This identifier is used to filter the subscriptions based on the product associated with
 * the subscription plan
 * :type appIdentifier: string
 * :param user: The `user` parameter in the `restoreSubscription` function represents the user for whom
 * the subscription needs to be restored. It contains information about the user, such as their `id`,
 * which is used to filter the subscriptions based on the user ID. This parameter is essential for
 * identifying the user and retrieving
 * :type user: User
 * :return: The `restoreSubscription` function returns a Promise that resolves to an object with three
 * properties: `code`, `status`, and `data`. The `code` property is a number, the `status` property is
 * a string indicating the status of the operation (in this case, 'success'), and the `data` property
 * contains the Subscription object that was retrieved based on the provided appIdentifier and user
 */


##  static String transactions = "/api/subscription";

/**
 * This TypeScript function creates a subscription for a user based on the provided package and price,
 * handling various checks and interactions with the payment service.
 *
 * :param createSubscriptionDto: The `createSubscriptionDto` parameter in the `create` method is an
 * object that contains data needed to create a new subscription. It likely includes properties such as
 * `packageID` and `priceID` which are used to identify the package and price for the subscription
 * :type createSubscriptionDto: CreateSubscriptionDto
 * :param user: The `user` parameter in the `create` function represents the user who is creating a
 * subscription. This user is an instance of the `User` class or type, and it contains information
 * about the user, such as their `id`, `customerId`, and other relevant details needed for creating a
 * subscription
 * :type user: User
 * :return: The function `create` is returning either an object containing the subscription data
 * (`subscription_obj`) if the subscription creation is successful, or a string indicating that the
 * subscription could not be created on Stripe if there is an issue during the process.
 */


##  static String createApprovedPayments = "/api/subscription/createApprovedPayments";

/**
 * The function `Approvedcreate` performs various checks and processes to create a subscription for an
 * approved product based on user and header information.
 *
 * :param CreateApprovedSubscriptionDto: CreateApprovedSubscriptionDto is an object containing data for
 * creating an approved subscription. It likely includes properties such as appIdentifier, packageID,
 * priceID, and other details required to set up a subscription for a user
 * :type CreateApprovedSubscriptionDto: CreateApprovedSubscriptionDto
 * :param HeaderDto: HeaderDto is an object containing key-value pairs that provide information about
 * the request being made. In the code snippet provided, the HeaderDto is used to compare the key with
 * the key stored in the database for a specific product approval. It is used to verify the
 * authenticity of the request and ensure that the
 * :type HeaderDto: HeaderDto2
 * :param user: The `user` parameter in the `Approvedcreate` function seems to represent the user who
 * is initiating the creation of an approved subscription. This user is likely authenticated and has
 * specific details associated with them, such as an `id` that is used to identify them in the system
 * :type user: User
 * :return: The function `Approvedcreate` returns different responses based on the conditions met
 * during its execution. Here are the possible return values:
 */

##  static String getCards = "/api/payment-methods";

/**
 * The `findAll` function retrieves payment methods associated with a specific user in descending
 * order.
 *
 * :param user: The `findAll` function takes a `user` object as a parameter. The function then uses the
 * `user.id` to find payment methods associated with that user in the database. The payment methods are
 * retrieved in descending order based on their `id` and returned as an object with a `data`
 * :type user: User
 * :return: An object is being returned with a property `data` that contains an array of payment
 * methods belonging to the specified user.
 */


##  static String paymentSheet = "/api/payment-methods/payment-sheet";

/**
 * The function `createNewSetupIntent` creates a new setup intent for a user with a Stripe customer ID
 * and returns the ephemeral key, customer ID, and setup intent client secret.
 *
 * :param user: The `createNewSetupIntent` function takes a `User` object as a parameter. The function
 * first checks if the `customerId` property of the user is not null. If it is null, it throws an
 * HttpException with a message prompting the user to verify their account first to attach payment
 * methods
 * :type user: User
 * :return: The `createNewSetupIntent` function returns an object with the following structure:
 * ```json
 * {
 *   "data": {
 *     "ephemeralKey": "<ephemeralKey value>",
 *     "customer": "<user.customerId value>",
 *     "setupIntent": "<setupIntent.client_secret value>"
 *   }
 * }
 * ```
 */

##  static String setDefault = '/api/payment-methods/';

/**
 * The function `setAsDefault` updates a user's default payment method both on Stripe and in the
 * database.
 *
 * :param id: The `id` parameter in the `setAsDefault` function is used to identify the specific
 * payment method that the user wants to set as default. It is a number that corresponds to the ID of
 * the payment method in the database
 * :type id: number
 * :param user: The `user` parameter in the `setAsDefault` function is an object that represents a
 * user. It likely contains properties such as `id` and `customerId`. This user object is used to
 * identify the user whose payment method is being set as default
 * :type user: User
 * :return: { message: 'Default payment method updated' }
 */

##  static String appDownloaded = "/api/users/device";

  /**
   * This TypeScript function creates user device data, checks if the data already exists, updates
   * download count in the product table, and saves new user app data.
   *
   * :param user: The `user` parameter in the `createUserDeviceData` function represents the user object
   * containing information about the user who is creating the device data.
   * :type user: User
   * :param data: The `data` parameter in the `createUserDeviceData` function seems to contain
   * information related to a user's device data. It includes fields such as `appIdentifier`, `deviceId`,
   * `countryCode`, `osVersion`, and `appVersion`. This data is used to create a new entry
   * :type data: UserDeviceData
   * :return: The function `createUserDeviceData` returns a Promise that resolves to either the newly
   * created user device data if it doesn't already exist in the database, or the existing user device
   * data if it already exists. If the user device data already exists, the function returns an object
   * with code 200, status 'success', and the existing data. If the user device data is newly created,
   * the function add the user device data.
   */


##  static String installedApps = '/api/users/apps';

/**
 * This TypeScript function retrieves user apps based on the user ID along with related product
 * information.
 *
 * :param userId: The `getUserApp` function is an asynchronous function that takes a `userId` parameter
 * of type `number`. It retrieves user apps from a repository based on the provided `userId` and
 * returns a Promise that resolves to the fetched apps. The function uses `await` to wait for the
 * asynchronous operation of
 * :type userId: number
 * :return: The `getUserApp` function is returning a Promise that resolves to an array of applications
 * associated with the user specified by the `userId`. The applications include related product
 * information such as icons and cover images.
 */


##  static String forgetPassword = '/api/users/forgot-password';

  /**
   * The `forgotPassword` function sends an OTP to the provided email for the purpose of resetting a
   * forgotten password.
   *
   * :param email: The `forgotPassword` function is an asynchronous function that takes an `email`
   * parameter of type string. This function sends an OTP (One-Time Password) to the provided email
   * address for the purpose of resetting a forgotten password. The OTP data is obtained by calling the
   * `sendOtp` function with
   * :type email: string
   * :return: { message: 'OTP sent to your email', data: otpData }
   */


##  static String resetPassword = '/api/users/reset-password';

/**
 * The function `resetPassword` asynchronously resets a user's password after verifying an OTP.
 *
 * :param email: The `email` parameter is a string that represents the email address of the user for
 * whom the password is being reset
 * :type email: string
 * :param otp: One Time Password (OTP) sent to the user's email for verification
 * :type otp: string
 * :param password: The `resetPassword` function is used to reset a user's password. The `password`
 * parameter is the new password that the user wants to set for their account. This password will be
 * hashed using the `PasswordHashEngine` before being saved in the database
 * :type password: string
 * :return: { message: 'Password reset successfully' }
 */




