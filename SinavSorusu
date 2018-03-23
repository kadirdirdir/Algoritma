package sinav;

import java.awt.BorderLayout;
import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JPanel;
import javax.swing.border.EmptyBorder;
import javax.swing.JButton;
import java.awt.Color;
import java.awt.event.ActionListener;
import java.util.Random;
import java.awt.event.ActionEvent;
import javax.swing.JList;
import javax.swing.AbstractListModel;

public class Kadir extends JFrame {

	private JPanel contentPane;

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					Kadir frame = new Kadir();
					frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the frame.
	 */
	public Kadir() {
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setBounds(100, 100, 400, 400);
		contentPane = new JPanel();
		contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));
		contentPane.setLayout(new BorderLayout(0, 0));
		setContentPane(contentPane);
		JList list = new JList();
		list.setModel(new AbstractListModel() {
			String[] values = new String[] {"50'den büyük sayılar="};
			public int getSize() {
				return values.length;
			}
			public Object getElementAt(int index) {
				return values[index];
			}
		});
		contentPane.add(list, BorderLayout.WEST);
	
		
		JList list_1 = new JList();
		list_1.setModel(new AbstractListModel() {
			String[] values = new String[] {"50'den küçük sayılar="};
			public int getSize() {
				return values.length;
			}
			public Object getElementAt(int index) {
				return values[index];
			}
		});
		contentPane.add(list_1, BorderLayout.EAST);
		
		JButton btnSayIinTklaynz = new JButton("Rastgele sayı için tıkla.");
		btnSayIinTklaynz.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				Random rstgle= new Random();
				int sayimiz = rstgle.nextInt(100);
				String kdr = Integer.toString(sayimiz);
				if(sayimiz>50) {
					list.add(kdr);
				}
				else if(sayimiz <= 50) {
					list_1.add(kdr);
				}
				
				
			}
		});
		btnSayIinTklaynz.setForeground(Color.RED);
		contentPane.add(btnSayIinTklaynz, BorderLayout.NORTH);
		
		
	}

}
