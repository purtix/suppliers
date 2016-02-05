## Hotel Request By City

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
		<SearchHotelPriceRequest>
			<ItemDestination DestinationType="city" DestinationCode="AMS" />
			<ImmediateConfirmationOnly />
			<PeriodOfStay>
				<CheckInDate>2003-09-30</CheckInDate>
				<Duration>4</Duration>
			</PeriodOfStay>
			<IncludeRecommended/>
			<IncludePriceBreakdown/>
			<IncludeChargeConditions/>
			<ExcludeChargeableItems>
				<CancellationDeadlineHours>72</CancellationDeadlineHours>
			</ExcludeChargeableItems>
			<Rooms>
				<Room Code="DB" NumberOfRooms="1">
					<ExtraBeds>
						<Age>5</Age>
					</ExtraBeds>
				</Room>
				<Room Code="TB" NumberOfCots="2">
					<ExtraBeds>
						<Age>10</Age>
					</ExtraBeds>
				</Room>
				<Room Code="SB" />
			</Rooms>
			<StarRating MinimumRating="true">3</StarRating>
			<LocationCode>G1</LocationCode>
			<FacilityCodes>
				<FacilityCode>*AC</FacilityCode>
				<FacilityCode>*LS</FacilityCode>
			</FacilityCodes>
			<OrderBy>pricelowtohigh</OrderBy>
			<NumberOfReturnedItems>10</NumberOfReturnedItems>
		</SearchHotelPriceRequest>
	</RequestDetails>
</Request>
```