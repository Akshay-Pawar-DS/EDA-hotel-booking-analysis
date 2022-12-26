# EDA-hotel-booking-analysis

## Introduction :
  The tourism industry is one of the industries that are most affected by the Covid-19 pandemic, specifically, the hotel industry. With travel restrictions, according to research conducted by Mckinsey in 2020, the rate of hotel bookings has been deeply decreased, it makes investors of the industry very pessimistic.To deal with this, hotel owners need to operate their operations efficiently to increase revenue so they can 'survive' from this pandemic. Therefore, we will carry out Exploratory Data Analysis with the 'Hotel Booking Demand' database to find out what can be improved from a hotel operation.

## Approach:

### Data Cleaning and Feature Engineering:

 (1) Removing Duplicate rows:

All duplicate rows were dropped.

(2) Handling null values:

Null values in columns company and agent were replaced by 0.
Null values in column country were replaced by 'others'.
Null values in column children were replaced by the mean of the column.

(3) Converting columns to appropriate data types:

Changed data type of children, company, agent to int type.
Changed data type of reservation_status_date to date type.

(4) Removing outliers:

One outlier was found in the adr column. Simply dropped it.

(5) Creating new columns:

Created new column total_stay by adding stays_in_weekend_nights+stays_in_week_nights.
Created new column total_people by adding adults+children+babies.

### Exploratory Data Analysis:

Performed EDA and tried answering the following questions:

 Q1) Which agent makes the most no. of bookings?
 
 Q2) Which room type is in most demand and which room type generates the highest adr?
 
 Q3) Which meal type is the  most preffered meal of customers?
 
 Q4) What is the percentage of bookings in each hotel?
 
 Q5) Which hotel seems to make more revenue?
 
 Q6) Which hotel has a higher lead time?
 
 Q7) What is preferred stay length in each hotel?
 
 Q8) Which hotel has longer waiting time?
 
 Q9) Which hotel has higher bookings cancellation rate?
 
 Q10) Which hotel has high chance that its customer will return for another stay?
 
 Q11) Which is the most common channel for booking hotels?
 
 Q12) Which channel is mostly used for early booking of hotels?
 
 Q13) Which distribution channel brings better revenue generating deals for hotels?
 
 Q14) Which significant distribution channel has highest cancellation percentage?
 
 Q15) From where the most guests are coming? 
 
 Q16) How long do people stay at the hotels?
 
Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:

- Bar Plot.
- Histogram.
- Scatter Plot.
- Pie Chart.
- Line Plot.
- Heatmap.
- Box Plot

#### Univariate Analysis:

Performed univariate analysis and made following conclusions:

 1) Agent no. 9 has made most no. of bookings.
 
 2) Most demanded room type is A, but better adr generating rooms H, G and C. Hotels should increase the no. of room types A and H to maximise revenue.
 
 3) Most popular meal type is BB(Bed and Breakfast).
 
 4) Around 60% bookings are for City hotel and 40% bookings are for Resort hotel, therefore City Hotel is busier than Resort hotel.
 
 #### Bivariate Analysis:
 Performed Bivariate analysis and made following conclusions:
 
 5) Avg adr of Resort hotel is slightly lower than that of City hotel. Hence, City hotel seems to be making slightly more revenue.
 6) City hotel has slightly higher median lead time. Also median lead time is significantly higher in each case, this means customers generally plan their hotel visits way to early.
 7) Most common stay length is less than 4 days and generally people prefer City hotel for short stay, but for long stays, Resort Hotel is preferred.
 8) City hotel has significantly longer waiting time, hence City Hotel is much busier than Resort Hotel.
 9) Almost 30 % of City Hotel bookings got canceled.
 10) Both hotels have very small percentage that customer will repeat, but Resort hotel has slightly higher repeat % than City Hotel.
 11) TA/TO is the most common channel for booking hotels
 12) TA/TO is mostly used for planning Hotel visits ahead of time. But for sudden visits other mediums are most preferred.
 13) GDS channel brings higher revenue generating deals for City hotel, in contrast to that most bookings come via TA/TO. City Hotel can work to increase outreach on GDS channels to get more higher revenue generating deals.Resort hotel has more revnue generating deals by direct and TA/TO channel. Resort Hotel need to increase outreach on GDS channel to increase revenue.
 14) TA/TO has highest booking cancellation %. Therefore, a booking via TA/TO is 30% likely to get cancelled.
 15) Most guest are from Portugal and other Europian contries.
 16) Most people prefer to stay at the hotels of <=5 days
 
 ## DataSet Used:
 We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.

- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                     Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
- reservation_status_date: Date of making reservation status. 

 ## Conclusion :
- Around 60% bookings are for City hotel and 40% bookings are for Resort hotel, therefore City Hotel is busier
than Resort hotel. Also the overall adr of City hotel is slightly higher than Resort hotel.
- Mostly guests stay for less than 5 days in hotel and for longer stays Resort hotel is preferred.
- Both hotels have significantly higher booking cancellation rates and very few guests less than 3 % return for
another booking in City hotel. 5% guests return for stay in Resort hotel.
- Most of the guests came from european countries, with most no. of guest coming from Portugal.
- For hotels higher adr deals come via GDS channel, so hotels should increase their popularity on this channel.
- Guests use different channels for making bookings out of which most preferred way is TA/TO.
- Almost 30% of bookings via TA/TO are cancelled.
- Couples are the most common guests for hotels, hence hotels can plan services according to couples needs
to increase revenue.
- Not getting same room as reserved, longer lead time and waiting time do not affect cancellation of
bookings. Although different room allotment do lowers the adr.
- For customers, generally the longer stays (more than 15 days) can result in better deals in terms of low adr.

 
