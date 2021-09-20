# Location


### Get the last known location

1. Specifically, use the fused location provider to retrieve the device's last known location.
1. The fused location provider is one of the location APIs in Google Play services.

### Set up Google Play services

To access the fused location provider, your app's development project must include Google Play services. Download and install the Google Play services component via the SDK Manager and add the library to your project.

### Specify app permissions

Apps whose features use location services must request location permissions, depending on the use cases of those features.

### Create location services client

1. In your activity's onCreate() method, create an instance of the Fused Location Provider Client as the following code snippet shows.

```java
private FusedLocationProviderClient fusedLocationClient;
@Override
protected void onCreate(Bundle savedInstanceState) {
    // ...

    fusedLocationClient = LocationServices.getFusedLocationProviderClient(this);
}
```

1. The precision of the location returned by this call is determined by the permission setting you put in your app manifest, as described in the guide on how to request location permissions.

1. To request the last known location, call the getLastLocation()

1. The getLastLocation() method returns a Task that you can use to get a Location object with the latitude and longitude coordinates of a geographic location.
1. The location object may be null in the following situations
   - Location is turned off in the device settings
   - The device never recorded its location,
   - Google Play services on the device has restarted, and there is no active Fused Location Provider client that has requested location after the services restarted.

### Choose the best location estimate

1. getLastLocation() gets a location estimate more quickly and minimizes battery usage that can be attributed to your app.
1. getCurrentLocation() gets a fresher, more accurate location more consistently. However, this method can cause active location computation to occur on the device
1. If your app calls requestLocationUpdates(), your app can sometimes consume large amounts of power if location isn't available, or if the request isn't stopped correctly after obtaining a fresh location.