# Final Project Java


## API DOCS
``` 
SWAGGER JSON DOCS

{
    "swagger": "2.0",
    "info": {
        "description": "Api Documentation",
        "version": "1.0",
        "title": "Api Documentation",
        "termsOfService": "urn:tos",
        "contact": {},
        "license": {
            "name": "Apache 2.0",
            "url": "http://www.apache.org/licenses/LICENSE-2.0"
        }
    },
    "host": "localhost:8080",
    "basePath": "/",
    "tags": [
        {
            "name": "agency-controller",
            "description": "Agency Controller"
        },
        {
            "name": "trip-schedule-controller",
            "description": "Trip Schedule Controller"
        },
        {
            "name": "transportation-reservation-controller",
            "description": "Transportation Reservation Controller"
        },
        {
            "name": "ticket-controller",
            "description": "Ticket Controller"
        },
        {
            "name": "auth-controller",
            "description": "Auth Controller"
        },
        {
            "name": "test-controller",
            "description": "Test Controller"
        },
        {
            "name": "bus-controller",
            "description": "Bus Controller"
        },
        {
            "name": "user-controller",
            "description": "User Controller"
        },
        {
            "name": "trip-controller",
            "description": "Trip Controller"
        },
        {
            "name": "stop-controller",
            "description": "Stop Controller"
        }
    ],
    "paths": {
        "/api/auth": {
            "post": {
                "tags": [
                    "auth-controller"
                ],
                "summary": "authenticateUser",
                "operationId": "authenticateUserUsingPOST",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "in": "body",
                        "name": "loginRequest",
                        "description": "loginRequest",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/LoginRequest"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                }
            }
        },
        "/api/test/admin": {
            "get": {
                "tags": [
                    "test-controller"
                ],
                "summary": "adminAccess",
                "operationId": "adminAccessUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "string"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                }
            }
        },
        "/api/test/all": {
            "get": {
                "tags": [
                    "test-controller"
                ],
                "summary": "allAccess",
                "operationId": "allAccessUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "string"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                }
            }
        },
        "/api/test/user": {
            "get": {
                "tags": [
                    "test-controller"
                ],
                "summary": "userAccess",
                "operationId": "userAccessUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "string"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/agency/": {
            "get": {
                "tags": [
                    "agency-controller"
                ],
                "summary": "getAll",
                "operationId": "getAllUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "post": {
                "tags": [
                    "agency-controller"
                ],
                "summary": "addAgency",
                "operationId": "addAgencyUsingPOST",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "in": "body",
                        "name": "agencyRequest",
                        "description": "agencyRequest",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/AgencyRequest"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/agency/{id}": {
            "get": {
                "tags": [
                    "agency-controller"
                ],
                "summary": "getAgencyById",
                "operationId": "getAgencyByIdUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "put": {
                "tags": [
                    "agency-controller"
                ],
                "summary": "updateAgency",
                "operationId": "updateAgencyUsingPUT",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    },
                    {
                        "in": "body",
                        "name": "agencyDetail",
                        "description": "agencyDetail",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/AgencyRequest"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "delete": {
                "tags": [
                    "agency-controller"
                ],
                "summary": "deleteAgency",
                "operationId": "deleteAgencyUsingDELETE",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "204": {
                        "description": "No Content"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/bus/": {
            "get": {
                "tags": [
                    "bus-controller"
                ],
                "summary": "getAll",
                "operationId": "getAllUsingGET_1",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "post": {
                "tags": [
                    "bus-controller"
                ],
                "summary": "addBus",
                "operationId": "addBusUsingPOST",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "in": "body",
                        "name": "busRequest",
                        "description": "busRequest",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/BusRequest"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/bus/{id}": {
            "get": {
                "tags": [
                    "bus-controller"
                ],
                "summary": "getBusById",
                "operationId": "getBusByIdUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "put": {
                "tags": [
                    "bus-controller"
                ],
                "summary": "updateBus",
                "operationId": "updateBusUsingPUT",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    },
                    {
                        "in": "body",
                        "name": "busDetail",
                        "description": "busDetail",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/BusRequest"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "delete": {
                "tags": [
                    "bus-controller"
                ],
                "summary": "deleteBus",
                "operationId": "deleteBusUsingDELETE",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "204": {
                        "description": "No Content"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/reservation/bookticket": {
            "post": {
                "tags": [
                    "transportation-reservation-controller"
                ],
                "summary": "bookTicket",
                "operationId": "bookTicketUsingPOST",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "in": "body",
                        "name": "ticketRequest",
                        "description": "ticketRequest",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/TicketRequest"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                }
            }
        },
        "/api/v1/reservation/stops": {
            "get": {
                "tags": [
                    "transportation-reservation-controller"
                ],
                "summary": "getAllStops",
                "operationId": "getAllStopsUsingGET_1",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                }
            }
        },
        "/api/v1/reservation/tripsbystops": {
            "get": {
                "tags": [
                    "transportation-reservation-controller"
                ],
                "summary": "getTripsByStops",
                "operationId": "getTripsByStopsUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "sourceStop",
                        "in": "query",
                        "description": "sourceStop",
                        "required": true,
                        "type": "string"
                    },
                    {
                        "name": "destStop",
                        "in": "query",
                        "description": "destStop",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                }
            }
        },
        "/api/v1/reservation/tripschedules": {
            "get": {
                "tags": [
                    "transportation-reservation-controller"
                ],
                "summary": "getTripSchedules",
                "operationId": "getTripSchedulesUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "date",
                        "in": "query",
                        "description": "date",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                }
            }
        },
        "/api/v1/stop/": {
            "get": {
                "tags": [
                    "stop-controller"
                ],
                "summary": "getAllStops",
                "operationId": "getAllStopsUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "post": {
                "tags": [
                    "stop-controller"
                ],
                "summary": "addStop",
                "operationId": "addStopUsingPOST",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "in": "body",
                        "name": "stop",
                        "description": "stop",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/Stop"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/stop/code": {
            "get": {
                "tags": [
                    "stop-controller"
                ],
                "summary": "getStopByCode",
                "operationId": "getStopByCodeUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "code",
                        "in": "query",
                        "description": "code",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/stop/name": {
            "get": {
                "tags": [
                    "stop-controller"
                ],
                "summary": "getStopByName",
                "operationId": "getStopByNameUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "name",
                        "in": "query",
                        "description": "name",
                        "required": true,
                        "type": "string"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/stop/{id}": {
            "get": {
                "tags": [
                    "stop-controller"
                ],
                "summary": "getStopById",
                "operationId": "getStopByIdUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "put": {
                "tags": [
                    "stop-controller"
                ],
                "summary": "updateStop",
                "operationId": "updateStopUsingPUT",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    },
                    {
                        "in": "body",
                        "name": "stopDetail",
                        "description": "stopDetail",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/Stop"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "delete": {
                "tags": [
                    "stop-controller"
                ],
                "summary": "deleteStop",
                "operationId": "deleteStopUsingDELETE",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "204": {
                        "description": "No Content"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/ticket/": {
            "get": {
                "tags": [
                    "ticket-controller"
                ],
                "summary": "getAll",
                "operationId": "getAllUsingGET_2",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "post": {
                "tags": [
                    "ticket-controller"
                ],
                "summary": "addTicket",
                "operationId": "addTicketUsingPOST",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "in": "body",
                        "name": "ticketRequest",
                        "description": "ticketRequest",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/TicketRequest"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/ticket/{id}": {
            "get": {
                "tags": [
                    "ticket-controller"
                ],
                "summary": "getTicketById",
                "operationId": "getTicketByIdUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "delete": {
                "tags": [
                    "ticket-controller"
                ],
                "summary": "deleteTicket",
                "operationId": "deleteTicketUsingDELETE",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "204": {
                        "description": "No Content"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/trip/": {
            "get": {
                "tags": [
                    "trip-controller"
                ],
                "summary": "getAll",
                "operationId": "getAllUsingGET_3",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "post": {
                "tags": [
                    "trip-controller"
                ],
                "summary": "addTrip",
                "operationId": "addTripUsingPOST",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "in": "body",
                        "name": "tripRequest",
                        "description": "tripRequest",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/TripRequest"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/trip/{id}": {
            "get": {
                "tags": [
                    "trip-controller"
                ],
                "summary": "getTripById",
                "operationId": "getTripByIdUsingGET",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "put": {
                "tags": [
                    "trip-controller"
                ],
                "summary": "updateTrip",
                "operationId": "updateTripUsingPUT",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    },
                    {
                        "in": "body",
                        "name": "tripDetail",
                        "description": "tripDetail",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/TripRequest"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "delete": {
                "tags": [
                    "trip-controller"
                ],
                "summary": "deleteTrip",
                "operationId": "deleteTripUsingDELETE",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "204": {
                        "description": "No Content"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/tripSchedule/": {
            "get": {
                "tags": [
                    "trip-schedule-controller"
                ],
                "summary": "getAll",
                "operationId": "getAllUsingGET_4",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "post": {
                "tags": [
                    "trip-schedule-controller"
                ],
                "summary": "addTrip",
                "operationId": "addTripUsingPOST_1",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "in": "body",
                        "name": "tripScheduleRequest",
                        "description": "tripScheduleRequest",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/GetTripScheduleRequest"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/tripSchedule/{id}": {
            "get": {
                "tags": [
                    "trip-schedule-controller"
                ],
                "summary": "getTripById",
                "operationId": "getTripByIdUsingGET_1",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "put": {
                "tags": [
                    "trip-schedule-controller"
                ],
                "summary": "updateTrip",
                "operationId": "updateTripUsingPUT_1",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    },
                    {
                        "in": "body",
                        "name": "tripScheduleDetail",
                        "description": "tripScheduleDetail",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/GetTripScheduleRequest"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            },
            "delete": {
                "tags": [
                    "trip-schedule-controller"
                ],
                "summary": "deleteTrip",
                "operationId": "deleteTripUsingDELETE_1",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "name": "id",
                        "in": "path",
                        "description": "id",
                        "required": true,
                        "type": "integer",
                        "format": "int64"
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "204": {
                        "description": "No Content"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    }
                },
                "security": [
                    {
                        "apiKey": []
                    }
                ]
            }
        },
        "/api/v1/user/signup": {
            "post": {
                "tags": [
                    "user-controller"
                ],
                "summary": "registerUser",
                "operationId": "registerUserUsingPOST",
                "consumes": [
                    "application/json"
                ],
                "produces": [
                    "*/*"
                ],
                "parameters": [
                    {
                        "in": "body",
                        "name": "signUpRequest",
                        "description": "signUpRequest",
                        "required": true,
                        "schema": {
                            "$ref": "#/definitions/SignupRequest"
                        }
                    }
                ],
                "responses": {
                    "200": {
                        "description": "OK",
                        "schema": {
                            "type": "object"
                        }
                    },
                    "201": {
                        "description": "Created"
                    },
                    "401": {
                        "description": "Unauthorized"
                    },
                    "403": {
                        "description": "Forbidden"
                    },
                    "404": {
                        "description": "Not Found"
                    }
                }
            }
        }
    },
    "securityDefinitions": {
        "apiKey": {
            "type": "apiKey",
            "name": "Authorization",
            "in": "header"
        }
    },
    "definitions": {
        "AgencyRequest": {
            "type": "object",
            "properties": {
                "code": {
                    "type": "string"
                },
                "details": {
                    "type": "string"
                },
                "name": {
                    "type": "string"
                },
                "owner": {
                    "type": "integer",
                    "format": "int64"
                }
            }
        },
        "BusRequest": {
            "type": "object",
            "properties": {
                "agencyId": {
                    "type": "integer",
                    "format": "int64"
                },
                "capacity": {
                    "type": "integer",
                    "format": "int32"
                },
                "code": {
                    "type": "string"
                },
                "make": {
                    "type": "string"
                }
            }
        },
        "GetTripScheduleRequest": {
            "type": "object",
            "properties": {
                "available_seats": {
                    "type": "integer",
                    "format": "int32"
                },
                "tripDate": {
                    "type": "string"
                },
                "trip_detail": {
                    "type": "integer",
                    "format": "int64"
                }
            }
        },
        "LoginRequest": {
            "type": "object",
            "properties": {
                "password": {
                    "type": "string"
                },
                "username": {
                    "type": "string"
                }
            }
        },
        "SignupRequest": {
            "type": "object",
            "properties": {
                "email": {
                    "type": "string"
                },
                "firstName": {
                    "type": "string"
                },
                "lastName": {
                    "type": "string"
                },
                "mobileNumber": {
                    "type": "string"
                },
                "password": {
                    "type": "string"
                },
                "role": {
                    "type": "array",
                    "items": {
                        "type": "string"
                    }
                },
                "username": {
                    "type": "string"
                }
            }
        },
        "Stop": {
            "type": "object",
            "properties": {
                "code": {
                    "type": "string"
                },
                "detail": {
                    "type": "string"
                },
                "id": {
                    "type": "integer",
                    "format": "int64"
                },
                "name": {
                    "type": "string"
                }
            }
        },
        "TicketRequest": {
            "type": "object",
            "properties": {
                "cancellable": {
                    "type": "boolean"
                },
                "journeyDate": {
                    "type": "string"
                },
                "passegerId": {
                    "type": "integer",
                    "format": "int64"
                },
                "seatNumber": {
                    "type": "integer",
                    "format": "int32"
                },
                "tripScheduleId": {
                    "type": "integer",
                    "format": "int64"
                }
            }
        },
        "TripRequest": {
            "type": "object",
            "properties": {
                "agencyid": {
                    "type": "integer",
                    "format": "int64"
                },
                "busId": {
                    "type": "integer",
                    "format": "int64"
                },
                "destStopid": {
                    "type": "integer",
                    "format": "int64"
                },
                "fare": {
                    "type": "integer",
                    "format": "int32"
                },
                "journeyTime": {
                    "type": "integer",
                    "format": "int32"
                },
                "sourceStopId": {
                    "type": "integer",
                    "format": "int64"
                }
            }
        }
    }
}

```

SWAGGER UI DOCS
![alt text](https://github.com/ihsbramn/final_project_java_TanPutSan/blob/main/swagger.jpeg)

## Contributing

- Ikhsan Abdurachman
- Putri Ester
- Tania Arsha
