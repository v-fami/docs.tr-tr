---
title: Hataları İşleme
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Internet, WebRequest and WebResponse classes exceptions
- Status property
- WebExceptions class, about WebExceptions class
- Timeout enumeration member
- ConnectFailure enumeration member
- TrustFailure enumeration member
- WebRequest class, exceptions
- requesting data from Internet, error handling
- Success enumeration member
- receiving data, errors
- ProtocolError enumeration member
- downloading Internet resources, error handling
- WebResponse class, exceptions
- SendFailure enumeration member
- errors [.NET Framework], WebRequest and WebResponse classes exceptions
- sending data, errors
- response to Internet request, error handling
- NameResolutionFailure enumeration member
- KeepAliveFailure enumeration member
- network resources, WebRequest and WebResponse classes exceptions
- RequestCanceled enumeration member
- ReceiveFailure enumeration member
- ServerProtocolViolation enumeration member
- ConnectionClosed enumeration member
- SecureChannelFailure enumeration member
ms.assetid: 657141cd-5cf5-4fdb-a4b2-4c040eba84b5
ms.openlocfilehash: 26e2a25855485bdd19d30e8497d0f75b7d4432e0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61642730"
---
# <a name="handling-errors"></a>Hataları İşleme
<xref:System.Net.WebRequest> Ve <xref:System.Net.WebResponse> sınıflar her iki sistem özel durumlarını throw (gibi <xref:System.ArgumentException>) ve Web özel durumlar (hangi <xref:System.Net.WebException> tarafından oluşturulan <xref:System.Net.WebRequest.GetResponse%2A> yöntemi).  
  
 Her **WebException** içeren bir <xref:System.Net.WebException.Status%2A> arasında bir değer içeren özellik <xref:System.Net.WebExceptionStatus> sabit listesi. İnceleyebilirsiniz **durumu** özelliği oluşan hata belirlemek ve hatayı gidermek için uygun adımları atın.  
  
 Aşağıdaki tabloda olası değerleri açıklanmaktadır **durumu** özelliği.  
  
|Durum|Açıklama|  
|------------|-----------------|  
|ConnectFailure|Uzak Hizmet taşıma düzeyinde kurulamadı.|  
|ConnectionClosed|Bağlantıyı erken sonlandırdı.|  
|KeepAliveFailure|Sunucu Keep-alive üst bilgisi kümesiyle yapılan bağlantı kapatıldı.|  
|NameResolutionFailure|Ad hizmeti konak adı çözümlenemedi.|  
|ProtocolError|Sunucudan alınan yanıtı tamamlandı ancak protokol düzeyinde bir hata gösterilir.|  
|ReceiveFailure|Uzak sunucudan tam yanıtı alınmadı.|  
|RequestCanceled|İstek iptal edildi.|  
|SecureChannelFailure|Güvenli kanal bağlantısında hata oluştu.|  
|SendFailure|Uzak sunucuya tam bir istek gönderilemedi.|  
|ServerProtocolViolation|Sunucu yanıtı geçerli bir HTTP yanıt değildi.|  
|Başarılı|Herhangi bir hata ile karşılaşıldı.|  
|zaman aşımı|İçin isteği zaman aşımı içinde yanıt alınmadı.|  
|TrustFailure|Bir sunucu sertifikası doğrulanamadı.|  
|MessageLengthLimitExceeded|Bir isteği gönderirken belirtilen sınırı aşan bir ileti alındı veya bir yanıt sunucudan alma.|  
|Bekleniyor|İç zaman uyumsuz isteği bekliyor.|  
|PipelineFailure|Bu değer .NET Framework altyapısını destekler ve doğrudan kodunuzda kullanılması amaçlanmamıştır.|  
|ProxyNameResolutionFailure|Ad çözümleyici hizmetini proxy konak adı çözümlenemedi.|  
|Başvuruları|Bilinmeyen türde bir özel durum oluştu.|  
  
 Zaman **durumu** özelliği **WebExceptionStatus.ProtocolError**, **WebResponse** sunucu yanıtı içeren kullanılabilir. Protokol hatası gerçek kaynağını belirlemek için bu yanıtı inceleyebilirsiniz.  
  
 Aşağıdaki örnek catch gösterilmiştir bir **WebException**.  
  
```csharp  
try   
{  
    // Create a request instance.  
    WebRequest myRequest =   
    WebRequest.Create("http://www.contoso.com");  
    // Get the response.  
    WebResponse myResponse = myRequest.GetResponse();  
    //Get a readable stream from the server.   
    Stream sr = myResponse.GetResponseStream();  
  
    //Read from the stream and write any data to the console.  
    bytesread = sr.Read( myBuffer, 0, length);  
    while( bytesread > 0 )   
    {  
        for (int i=0; i<bytesread; i++) {  
            Console.Write( "{0}", myBuffer[i]);  
        }  
        Console.WriteLine();  
        bytesread = sr.Read( myBuffer, 0, length);  
    }  
    sr.Close();  
    myResponse.Close();  
}  
catch (WebException webExcp)   
{  
    // If you reach this point, an exception has been caught.  
    Console.WriteLine("A WebException has been caught.");  
    // Write out the WebException message.  
    Console.WriteLine(webExcp.ToString());  
    // Get the WebException status code.  
    WebExceptionStatus status =  webExcp.Status;  
    // If status is WebExceptionStatus.ProtocolError,   
    //   there has been a protocol error and a WebResponse   
    //   should exist. Display the protocol error.  
    if (status == WebExceptionStatus.ProtocolError) {  
        Console.Write("The server returned protocol error ");  
        // Get HttpWebResponse so that you can check the HTTP status code.  
        HttpWebResponse httpResponse = (HttpWebResponse)webExcp.Response;  
        Console.WriteLine((int)httpResponse.StatusCode + " - "  
           + httpResponse.StatusCode);  
    }  
}  
catch (Exception e)   
{  
    // Code to catch other exceptions goes here.  
}  
```  
  
```vb  
Try  
    ' Create a request instance.  
    Dim myRequest As WebRequest = WebRequest.Create("http://www.contoso.com")  
    ' Get the response.  
    Dim myResponse As WebResponse = myRequest.GetResponse()  
    'Get a readable stream from the server.   
    Dim sr As Stream = myResponse.GetResponseStream()  
  
    Dim i As Integer      
    'Read from the stream and write any data to the console.  
    bytesread = sr.Read(myBuffer, 0, length)  
    While bytesread > 0  
        For i = 0 To bytesread - 1  
            Console.Write("{0}", myBuffer(i))  
        Next i  
        Console.WriteLine()  
        bytesread = sr.Read(myBuffer, 0, length)  
    End While  
    sr.Close()  
    myResponse.Close()  
Catch webExcp As WebException  
    ' If you reach this point, an exception has been caught.  
    Console.WriteLine("A WebException has been caught.")  
    ' Write out the WebException message.  
    Console.WriteLine(webExcp.ToString())  
    ' Get the WebException status code.  
    Dim status As WebExceptionStatus = webExcp.Status  
    ' If status is WebExceptionStatus.ProtocolError,   
    '   there has been a protocol error and a WebResponse   
    '   should exist. Display the protocol error.  
    If status = WebExceptionStatus.ProtocolError Then  
        Console.Write("The server returned protocol error ")  
        ' Get HttpWebResponse so that you can check the HTTP status code.  
        Dim httpResponse As HttpWebResponse = _  
           CType(webExcp.Response, HttpWebResponse)  
        Console.WriteLine(CInt(httpResponse.StatusCode).ToString() & _  
           " - " & httpResponse.StatusCode.ToString())  
    End If  
Catch e As Exception  
    ' Code to catch other exceptions goes here.  
End Try  
```  
  
 Kullanan uygulamalar <xref:System.Net.Sockets.Socket> sınıfı throw <xref:System.Net.Sockets.SocketException> hataları Windows yuva olduğunda. <xref:System.Net.Sockets.TcpClient>, <xref:System.Net.Sockets.TcpListener>, Ve <xref:System.Net.Sockets.UdpClient> sınıfları üst kısmındaki yerleşiktir **yuva** sınıfı ve throw **SocketExceptions** de.  
  
 Olduğunda bir **SocketException** oluşturulur, **SocketException** sınıf kümelerini <xref:System.Net.Sockets.SocketException.ErrorCode%2A> özelliğini gerçekleşen son işletim sistemi Yuva hatası. Yuva hata kodları hakkında daha fazla bilgi için MSDN'de Winsock 2.0 API'sine hata kodu belgelerine bakın.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Özel durum işleme temelleri](../../../docs/standard/exceptions/exception-handling-fundamentals.md)
- [Veri İsteme](../../../docs/framework/network-programming/requesting-data.md)
