# Hello
EGIT
CHANGES
jhgjgk

package stock;

import java.util.ArrayList;
import java.util.Calendar;
import java.util.GregorianCalendar;
import java.util.List;
import java.util.Random;

public class GetRandom {
	public static void main(String[] args) {
		//List<String> list = new ArrayList<String>();
		String stockQuery = getStockQuery();
		System.out.println(stockQuery);
	}
	
	public static String getStockQuery() {
		String[] stockArray = {"NASDAQ-ACRX", "NASDAQ-ACET", "NASDAQ-AKAO", "NASDAQ-ACHN", "NASDAQ-ACIW", "NASDAQ-ACRS", "NASDAQ-ADTN", "NASDAQ-ADRO", "NASDAQ-AAAP", "NASDAQ-ADES", 
				"NASDAQ-AEIS", "NASDAQ-AEGR", "NASDAQ-AEGN", "NASDAQ-AGLE", "NASDAQ-AEHR", "NASDAQ-AGEN", "NASDAQ-AGRX", "NASDAQ-AGYS", 
				"NASDAQ-AGIO", "NASDAQ-AGFS", "NASDAQ-AGFSW", "NASDAQ-AIMT", "NASDAQ-AIRM", "NASDAQ-AIRT", "NASDAQ-ATSG", "NASDAQ-ALDX", "NASDAQ-ALXN", "NASDAQ-ALCO", 
				"NASDAQ-ALGN", "NASDAQ-ALIM", "NASDAQ-AMBA", "NASDAQ-AMCX", "NASDAQ-AMKR", "NASDAQ-AMPH", 
				"NASDAQ-AMSG", "NASDAQ-AMSGP", "NASDAQ-ASYS", "NASDAQ-AFSI", "NASDAQ-AMRS", "NASDAQ-ADI", "NASDAQ-ALOG", "NASDAQ-ABAC", "NASDAQ-ARDM", "NASDAQ-ARCW", 
				"NASDAQ-ABIO", "NASDAQ-AROW", "NASDAQ-BUFF", "NASDAQ-BHBK", "NASDAQ-BLUE", "NASDAQ-BKEP", "NASDAQ-BSFT", 
				"NASDAQ-BVSN", "NASDAQ-BYFC", "NASDAQ-BWEN", "NASDAQ-BRCD", "NASDQAQ-BRKL", "NASDAQ-CHY", "NASDAQ-CHI", "NASDAQ-CCD", "NASDAQ-CTRE", "NASDAQ-CKEC", 
				"NASDAQ-CVCO", "NASDAQ-CAVM", "NASDAQ-CBFV", "NASDAQ-CBOE", "NASDAQ-CDK", "NASDAQ-CDW", "NASDAQ-CHUBK", "NASDAQ-DISCK", "NASDAQ-DISH", "NASDAQ-DVCR", 
				"NASDAQ-DLHC", "NASDAQ-EGBN", "NASDAQ-EGLE", "NASDAQ-EGRX", "NASDAQ-ELNK", "NASDAQ-EWBC", "NASDAQ-EACQ", "NASDAQ-EACQU", "NASDAQ-EACQW", "NASDAQ-EML", 
				"NASDAQ-EVBS", "NASDAQ-EVGBC", "NASDAQ-EXTR", "NASDAQ-EENX", "NASDAQ-EFBC", "NASDAQ-EFBCW", "NASDAQ-EFIN", 
				"NASDAQ-GLPG","NASDAQ-GALT","NASDAQ-GALTU","NASDAQ-GALTW","NASDAQ-GALE","NASDAQ-GLMD","NASDAQ-GLPI","NASDAQ-GPIC","NASDAQ-GRMN",
				"NASDAQ-GARS","NASDAQ-GCTS","NASDAQ-GEMP","NASDAQ-GENC","NASDAQ-GNCMA","NASDAQ-GFN","NASDAQ-GFNCP","NASDAQ-GFNSL","NASDAQ-GENE",
				"NASDAQ-GNMK","NASDAQ-GNCA","NASDAQ-GHDX","NASDAQ-GNST","NASDAQ-GNTX","NASDAQ-GLADO", "NYSE-MMM", "NYSE-WBAI", "NYSE-WUBA", "NYSE-AHC", 
				"NYSE-ATEN", "NYSE-AAC", "NYSE-AIR", "NYSE-AAN", "NYSE-ABB", "NYSE-ABT", "NYSE-ABBV", "NYSE-ANF", "NYSE-GCH", "NYSE-JEQ", "NYSE-SGF", "NYSE-ABM", 
				"NYSE-AKR", "NYSE-ACN", "NYSE-ACCO", "NYSE-ACW", "NYSE-ATV", "NYSE-ATU", "NYSE-AYI", "NYSE-ADX", "NYSE-PEO", "NYSE-AGRO", "NYSE-ADPT", "NYSE-AAP", 
				"NYSE-CLW", "NYSE-CLF", "NYSE-CLX", "NYSE-CLD", "NYSE-MYCC", "NYSE-CMS", "NYSE-CMS^B", "NYSE-CNA", "NYSE-CNHI", "NYSE-CNO", "NYSE-CEO", "NYSE-CNXC", "NYSE-COH", 
				"NYSE-COR^A", "NYSE-GLW", "NYSE-GYC", "NYSE-OFC", "NYSE-OFC^L", "NYSE-CXW", "NYSE-CZZ", "NYSE-CMRE", "NYSE-CMRE^B", "NYSE-CMRE^C", "NYSE-CMRE^D", 
				"NYSE-COTV", "NYSE-COT", "NYSE-COTY", "NYSE-CFC^B", "NYSE-CUZ", "NYSE-CVA", "NYSE-CPF", "NYSE-CPL", "NYSE-CR", "NYSE-CRD.A", "NYSE-CRD.B", "NYSE-BAP", 
				"NYSE-CYS", "NYSE-CYS^A", "NYSE-CYS^B", "NYSE-DHI", "NYSE-CB", "NYSE-DAN", "NYSE-DHR", "NYSE-DAC", "NYSE-DQ", "NYSE-DRI", "NYSE-DAR", "NYSE-DVA", "NYSE-DPM", 
				"NYSE-DCT", "NYSE-DDR", "NYSE-DDR^J", "NYSE-DDR^K", "NYSE-DF", "NYSE-DECK", "NYSE-DE", "NYSE-DEX", "NYSE-DDF", "NYSE-DKL", "NYSE-DK", "NYSE-DLPH", 
				"NYSE-DAL", "NYSE-DEL", "NYSE-DLX", "NYSE-DMD", "NYSE-DNR", "NYSE-DKT", "NYSE-DB", "NYSE-DTK", "NYSE-DXB", "NYSE-DVN", "NYSE-DV", "NYSE-DHX", "NYSE-DHT", 
				"NYSE-DEO", "NYSE-DO", "NYSE-DRII", "NYSE-DRH", "NYSE-DSX", "NYSE-DSX^B", "NYSE-DSXN", "NYSE-DKS", "NYSE-DBD", "NYSE-DLR", "NYSE-DLR^E.CL", "NYSE-DLR^F", 
				"NYSE-DLR^G", "NYSE-DLR^H", "NYSE-DLR^I", "NYSE-DGI", "NYSE-DDS", "NYSE-DDT", "NYSE-DIN", "NYSE-DPLO", "NYSE-DFS", "NYSE-DFS^B", "NYSE-DRA", "NYSE-DNI", 
				"NYSE-DTF", "NYSE-DUC", "NYSE-DUK", "NYSE-DUKH", "NYSE-DRE", "NYSE-DNB", "NYSE-DFT", "NYSE-DFT^C", "NYSE-DHG", "NYSE-DY", "NYSE-DLNG", "NYSE-DLNG^A", 
				"NYSE-ENZ", "NYSE-EOG", "NYSE-EPE", "NYSE-EPAM", "NYSE-EPR", "NYSE-EPR^C", "NYSE-EPR^E", "NYSE-EPR^F", "NYSE-EQT", "NYSE-EQGP", "NYSE-EQM", "NYSE-EFX", 
				"NYSE-LLL", "NYSE-LQ", "NYSE-LH", "NYSE-LADR", "NYSE-LDR", "NYSE-LCI", "NYSE-LPI", "NYSE-LVS", "NYSE-LHO", "NYSE-LHO^H", "NYSE-LHO^I", "NYSE-LHO^J", "NYSE-LFL", "NYSE-LDF", 
				"NYSE-LGI", "NYSE-LAZ", "NYSE-LOR", "NYSE-LZB", "NYSE-LEA", "NYSE-LEE", "NYSE-BWG", "NYSE-LM", "NYSE-LMHA", "NYSE-LMHB", "NYSE-LEG", "NYSE-CVB", "NYSE-JBK", "NYSE-KCC", "NYSE-KTH", 
				"NYSE-WLH", "NYSE-LYB", "NYSE-MTB", "NYSE-MTB.WS", "NYSE-MTB^", "NYSE-MTB^C", "NYSE-MDC", "NYSE-MHO", "NYSE-MHO^A", "NYSE-MAC", "NYSE-CLI", "NYSE-MGU", "NYSE-MIC", "NYSE-MFD", 
				"NYSE-BMA", "NYSE-M", "NYSE-MCN", "NYSE-MSP", "NYSE-MMP", "NYSE-MGA", "NYSE-MX", "NYSE-MH^A", "NYSE-MH^C", "NYSE-MHLA", "NYSE-MHNB", "NYSE-MHNC", "NYSE-MAIN", "NYSE-MSCA", "NYSE-MMD", 
				"NYSE-MNK", "NYSE-MZF", "NYSE-MANU", "NYSE-MTW", "NYSE-MFS", "NYSE-MN", "NYSE-MAN", "NYSE-MFC", "NYSE-MRO", "NYSE-MPC", "NYSE-MMI", "NYSE-MCS", "NYSE-MRIN", "NYSE-MHG", "NYSE-MPX", 
				"NYSE-HZO", "NYSE-MKL", "NYSE-VAC", "NYSE-MMC", "NYSE-MLM", "NYSE-MAS", "NYSE-DOOR", "NYSE-MTZ", "NYSE-MA", "NYSE-MTDR", "NYSE-MTRN", "NYSE-MATX", "NYSE-MLP", "NYSE-MMS", "NYSE-MXL", 
				"NYSE-NVRO", "NYSE-HYB", "NYSE-GF", "NYSE-NWHM", "NYSE-IRL", "NYSE-NEWM", "NYSE-NMFC", "NYSE-EDU", "NYSE-NEWR", "NYSE-NRZ", "NYSE-SNR", "NYSE-NWY", "NYSE-NYCB", "NYSE-NYCB^U", 
				"NSE-ABB", "NSE-APOLLOHOSP", "NSE-ASHOKLEY", "NSE-BAJFINANCE", "NSE-BAJAJFINSV", "NSE-BEL", "NSE-BHARATFORG", "NSE-BRITANNIA", "NSE-CADILAHC", "NSE-CAIRN", 
				"NSE-CASTROLIND", "NSE-COLPAL", "NSE-CONCOR", "NSE-CUMMINSIND", "NSE-DLF", "NSE-DABUR", "NSE-DIVISLAB", "NSE-EMAMILTD", "NSE-GSKCONS", "NSE-GLAXO", 
				"NSE-GLENMARK", "NSE-GODREJCP", "NSE-HINDPETRO", "NSE-HINDZINC", "NSE-IBULHSGFIN", "NSE-IOC", "NSE-JSWSTEEL", "NSE-LICHSGFIN", "NSE-MARICO", "NSE-MOTHERSUMI", 
				"NSE-NHPC", "NSE-NMDC", "NSE-OIL", "NSE-OFSS", "NSE-PIDILITIND", "NSE-PFC", "NSE-PGHH", "NSE-PNB", "NSE-RCOM", "NSE-RECLTD", "NSE-SHREECEM", "NSE-SRTRANSFIN", 
				"NSE-SIEMENS", "NSE-SAIL", "NSE-TITAN", "NSE-TORNTPHARM", "NSE-UPL", "NSE-UBL", "NSE-MCDOWELL-N", "NSE-VEDL"};

			String[] sideArray = {"Sell", "Buy"};
			String[] statusArray = {"Cancelled", "Pending"};
			System.out.println(stockArray.length-50);
			String selectSide = sideArray[getBetween(0, sideArray.length-1)];
			
			GregorianCalendar selectOrderCal = getOrderDate();
			GregorianCalendar selectSettleCal = getSettleDate(selectOrderCal);
			String selectOrderDate = ""+selectOrderCal.get(Calendar.YEAR)+"-"+
					""+selectOrderCal.get(Calendar.MONTH)+"-"+
					""+selectOrderCal.get(Calendar.DATE)+" "+
					""+selectOrderCal.get(Calendar.HOUR)+":"+
					""+selectOrderCal.get(Calendar.MINUTE)+":"+
					""+selectOrderCal.get(Calendar.SECOND);
			String selectSettleDate = ""+selectSettleCal.get(Calendar.YEAR)+"-"+
					""+selectSettleCal.get(Calendar.MONTH)+"-"+
					""+selectSettleCal.get(Calendar.DATE)+" "+
					""+selectSettleCal.get(Calendar.HOUR)+":"+
					""+selectSettleCal.get(Calendar.MINUTE)+":"+
					""+selectSettleCal.get(Calendar.SECOND);
			
			int stockIndex = getBetween(0, stockArray.length-1);
			String selectStock = stockArray[stockIndex];
			
			String selectStatus = statusArray[getBetween(0, statusArray.length-1)];
			int selectVolume = getBetween(1, 100);
			int selectQuantity = getBetween(1, selectVolume);
			
			double selectPrice;
			
			if (stockIndex < 364)
				selectPrice = (double)getBetween(100, 70000)/100;
			else
				selectPrice = (double)getBetween(7000, 2300000)/100;
			
			return "UPDATE table VALUES ('"+selectSide+"', '"+selectOrderDate+"', '"
					+selectSettleDate+"', '"+selectStatus+"', '"+selectStock+"', '"+selectQuantity
					+ "', '"+selectVolume+"', '"+selectPrice+"')";
	}
	
	public static GregorianCalendar getOrderDate() {
		GregorianCalendar gc = new GregorianCalendar();
		int year = getBetween(2010, 2015);
		int month = getBetween(1, 12);
		int day = getBetween(1, gc.getActualMaximum(Calendar.DAY_OF_MONTH));
		int hour = getBetween(0, 12);
		int minute = getBetween(0, 59);
		int second = getBetween(0, 59);
		gc.set(year, month, day, hour, minute, second);
		return gc;
	}
			
	public static GregorianCalendar getSettleDate(GregorianCalendar gcOrder) {
		GregorianCalendar gc = new GregorianCalendar();
		int year = getBetween(gcOrder.get(Calendar.YEAR), 2015);
		int month = getBetween(gcOrder.get(Calendar.MONTH), 12);
		int date = getBetween(gcOrder.get(Calendar.DAY_OF_MONTH), gc.getActualMaximum(Calendar.DAY_OF_MONTH));
		int hour = getBetween(gcOrder.get(Calendar.HOUR), 12);
		int minute = getBetween(gcOrder.get(Calendar.MINUTE), 59);
		int second = getBetween(gcOrder.get(Calendar.SECOND), 59);
		gc.set(year, month, date, hour, minute, second);
		return gc;
	}
	
	public static int getBetween(int start, int end) {
		Random randomizer = new Random();
		return randomizer.nextInt(end - start + 1) + start;
	}
}
