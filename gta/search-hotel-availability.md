# Search Hotel Availability

## Overview

1. All requests will need to be sent in a SYNCHRONOUS mode; any requests send in an ASYNCHRONOUS mode will return an error.
2. The Search Hotel Availability provides the client with the ability to search for available hotel rooms through the API.
3. Please note that this request is not available for newly set up clients.

## Example XML Search Hotel Availability request

The XML message below gives a sample of the expected elements needed by the API to execute a Search Hotel Availability Request.

```
<?xml version="1.0" encoding="UTF-8" ?>
<Request>
	<Source>
		<RequestorID Client="1479" EMailAddress="client@net.com" Password="xxx" />
		<RequestorPreferences Language="en" Currency="GBP" Country="GB">
			<RequestMode>SYNCHRONOUS</RequestMode>
		</RequestorPreferences>
	</Source>
	<RequestDetails>
		<SearchHotelAvailabilityRequest>
			<ItemDestination DestinationType="city" DestinationCode="AMS" />
			<ImmediateConfirmationOnly />
			<PeriodOfStay>
				<CheckInDate>2005-03-11</CheckInDate>
				<Duration>14</Duration>
			</PeriodOfStay>
			<Rooms>
				<Room
					Code="TB"
					NumberOfRooms="1"
					NumberOfCots="2"
					ExtraBed="true"
					NumberOfExtraBeds="2" />
			</Rooms>
			<StarRating MinimumRating="true">3</StarRating>
			<LocationCode>G1</LocationCode>
			<FacilityCodes>
				<FacilityCode>*SO</FacilityCode>
				<FacilityCode>*TE</FacilityCode>
			</FacilityCodes>
		</SearchHotelAvailabilityRequest>
	</RequestDetails>
</Request>
```

## Example XML Search Hotel Availability response

The XML message below gives a sample of that given by the API in response to a Search Hotel Availability Request.

```
<?xml version="1.0" encoding="UTF-8" ?>
<Response>
	<ResponseDetails Language="en">
		<SearchHotelAvailabilityResponse>
			<HotelDetails>
				<Hotel>
					<City Code="AMS"><![CDATA[ Amsterdam ]]></City>
					<Item Code="CAN"><![CDATA[ Canal Crown ]]></Item>
					<RoomAvailability>
						<Availability>
							<DateRange>
								<FromDate>2005-03-11</FromDate>
								<ToDate>2005-03-15</ToDate>
							</DateRange>
							<Confirmation Code="IM"><![CDATA[AVAILABLE]]></Confirmation>
						</Availability>
						<Availability>
							<DateRange>
								<FromDate>2005-03-16</FromDate>
								<ToDate>2005-03-16</ToDate>
							</DateRange>
							<Confirmation Code="CL"><![CDATA[Closed]]></Confirmation>
						</Availability>
						<Availability>
							<DateRange>
								<FromDate>2005-03-17</FromDate>
								<ToDate>2005-03-21</ToDate>
							</DateRange>
							<Confirmation Code="OR"><![CDATA[On Request]]></Confirmation>
						</Availability>
					</RoomAvailability>
				</Hotel>
			</HotelDetails>
		</SearchHotelAvailabilityResponse>
	</ResponseDetails>
</Response>
```