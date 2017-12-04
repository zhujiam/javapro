# javapro


import java.time.LocalDate;

import javafx.beans.property.ObjectProperty;
import javafx.beans.property.SimpleDoubleProperty;
import javafx.beans.property.SimpleObjectProperty;
import javafx.beans.property.SimpleStringProperty;

public final class earthQuake {
	// ��������
    private final SimpleDoubleProperty longitude = new SimpleDoubleProperty();
    private final SimpleDoubleProperty latitude = new SimpleDoubleProperty();
    private final SimpleDoubleProperty magnitude = new SimpleDoubleProperty();
    private final ObjectProperty<LocalDate> date = new SimpleObjectProperty<>();
    private final SimpleStringProperty country = new SimpleStringProperty();
        // ������
        public earthQuake(){
        	
        }
        
        public earthQuake(Double longitude, Double latitude, Double magnitude, String country, LocalDate date){
        	this.longitude.set(longitude);
        	this.latitude.set(latitude);
        	this.magnitude.set(magnitude);
        	this.country.set(country);
        	this.date.set(date);
        }
   
    // longitude property
        public final Double getLongitude(){
        	return longitude.get();
        }
        public final void setLongitude(Double longitude){
        	longitudeProperty().set(longitude);
        }
		public final SimpleDoubleProperty longitudeProperty() {
			return longitude;
		}
    
   // latitude property
		public final Double getLatitude(){
			return latitude.get();
		}
		public final void setLatitude(Double latitude){
			latitudeProperty().set(latitude);
		}
		public final SimpleDoubleProperty latitudeProperty() {
			return latitude;
		}
   
   // Magnitude property
		public final Double getMagnitude(){
			return magnitude.get();
		}
		public final void setMagnitude(Double magnitude){
			magnitudeProperty().set(magnitude);
		}
		public final SimpleDoubleProperty magnitudeProperty() {
			return magnitude;
		}
   
   // Date property
		public final LocalDate getDate(){
			return date.get();
		}
		public final void setDate(LocalDate localdate){
			dateProperty().set(localdate);
		}
		public ObjectProperty<LocalDate> dateProperty() {
			return date;
		}
   
  // Country property
		public final String getCountry() {
			return country.get();
		}
		public final void setCountry(String country){
			countryProperty().set(country);
		}
        public final SimpleStringProperty countryProperty(){
        	return country;
        }
     
}
