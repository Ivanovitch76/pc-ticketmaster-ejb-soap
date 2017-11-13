package be.steformations.pc.ticketmaster.soap;

import be.steformations.pc.ticketmaster.common.beans.Booking;
import be.steformations.pc.ticketmaster.common.beans.Show;
import be.steformations.pc.ticketmaster.common.service.TicketMasterService;
import be.steformations.pc.ticketmaster.ejb.EjbTicketMasterService;

@javax.ejb.Singleton
@javax.ejb.Startup
@javax.jws.WebService(
	endpointInterface="be.steformations.pc.ticketmaster.common.service.TicketMasterService",
	targetNamespace="be.steformations.pc.ticketmaster",
	serviceName="SoapTicketMasterService"
)
public class SoapTicketMasterService implements TicketMasterService {
	
	@javax.ejb.EJB
	private EjbTicketMasterService ejbService;
	
	@Override
	public Show createShow(String title, int year, int month, int day, int hour, int minutes, int venue) {
		return this.ejbService.createShow(title, year, month, day, hour, minutes, venue);
	}

	@Override
	public Booking createBooking(int show, int client) {
		return this.ejbService.createBooking(show, client);
	}

}
