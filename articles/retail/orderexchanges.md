<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="orderexchanges.md" target-language="ar-SA">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>orderexchanges.ba78aa.43571099727830e81c41416b6fe250dba398b3f8.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>43571099727830e81c41416b6fe250dba398b3f8</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\orderexchanges.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Configure and process an exchange on a return order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">تكوين ومعالجة عملية استبدال في أمر إرجاع</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to configure an exchange on a return in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">يشرح هذا الموضوع كيفية تكوين عملية استبدال في أمر إرجاع في Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Configure and process an exchange on a return order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">تكوين ومعالجة عملية استبدال في أمر إرجاع</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In previous versions of Microsoft Dynamics 365 for Retail, returns against customer orders were processed by using the return order document in Retail Headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">في الإصدارات السابقة من Microsoft Dynamics 365 for Retail، كانت معالجة المرتجعات في مقابل أوامر العملاء تتم باستخدام مستند أمر الإرجاع في Retail Headquarters.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>However, the return order document can be used to process only products that are being returned.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ومع ذلك، يمكن استخدام مستند أمر الإرجاع لمعالجة المنتجات المرتجعة فقط.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The returned products are indicated by a negative quantity on the return order lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">يُشار إلى المنتجات المرتجعة بكمية سالبة في بنود أمر الإرجاع.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>By contrast, sales are indicated by a positive quantity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">وبطريقة مغايرة، يُشار إلى المبيعات بكمية موجبة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>However, the return order document doesn't support positive quantities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ومع ذلك، لا يدعم مستند أمر الإرجاع الكميات الموجبة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">وبسبب هذا القيد، لم تدعم الإصدارات السابقة من Retail السيناريوهات حيث كانت عمليات الاستبدال تتم فقط باستخدام مستند أمر الإرجاع.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>However, functionality has been added to support scenarios where exchanges are done on return orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ومع ذلك، تمت إضافة وظيفة لدعم السيناريوهات حيث تتم عمليات الاستبدال على الأوامر المرتجعة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Retail now uses the sales order document instead of the return order document to process these types of transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">يستخدم Retail الآن مستند أمر المبيعات بدلاً من مستند أمر الإرجاع لمعالجة هذه الأنواع من الحركات.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Configure Retail to support exchanges on return orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">تكوين Retail لدعم عمليات الاستبدال على أوامر الإرجاع</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Follow these steps to configure the system to support exchanges on return orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">اتبع هذه الخطوات لتكوين النظام لدعم عمليات الاستبدال على أوامر الإرجاع.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail parameters<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">انتقل إلى <bpt id="p1">**</bpt>البيع بالتجزئة <ph id="ph1">\&gt;</ph> إعداد Headquarters <ph id="ph2">\&gt;</ph> المعلمات <ph id="ph3">\&gt;</ph> معلمات البيع بالتجزئة<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>On the <bpt id="p1">**</bpt>Customer orders<ept id="p1">**</ept> FastTab, set the <bpt id="p2">**</bpt>Process return orders as sales orders<ept id="p2">**</ept> option to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">على علامة التبويب السريعة <bpt id="p1">**</bpt>أوامر العملاء‬<ept id="p1">**</ept>، عيّن الخيار <bpt id="p2">**</bpt>معالجة أوامر الإرجاع كأوامر مبيعات<ept id="p2">**</ept> إلى <bpt id="p3">**</bpt>نعم<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Run the <bpt id="p1">**</bpt>Global configuration distribution schedule<ept id="p1">**</ept> job (<bpt id="p2">**</bpt>1110<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">شغّل وظيفة <bpt id="p1">**</bpt>جدول توزيع التكوين العمومي<ept id="p1">**</ept> (<bpt id="p2">**</bpt>1110<ept id="p2">**</ept>).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Make an exchange</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">إجراء عملية استبدال</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">بعد أن يتم تكوين النظام كما ورد في المقطع السابق، سيحدد مستخدم نقطة البيع (POS) أمر مبيعات أو فاتورة مبيعات لمعالجة عملية إرجاع، كما هو الحال في إصدارات Retail السابقة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ومع ذلك، بعد إضافة الأصناف المرتجعة إلى سلة التسوق، سيتمكن المستخدم من إضافة بنود مبيعات جديدة إلى سلة التسوق.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">بالنسبة إلى بنود المبيعات الجديدة هذه، يجب على المستخدم تحديد كافة السمات المطلوبة لمعالجة بند في أمر العميل.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>These attributes include the delivery method and fulfillment location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">تتضمن هذه السمات أسلوب التسليم وموقع التنفيذ.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The payment that is due for the transaction will be a net of the return order lines and sales order lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">سيكون الدفع المستحق للحركة عبارة عن قيمة صافية لبنود أمر الإرجاع وبنود أمر المبيعات.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail Headquarters, and the system will immediately invoice the return lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">عند تقديم الدفع للحركة، سيتم ترحيل أمر الإرجاع كمستند أمر مبيعات في Retail Headquarters، وسيقوم النظام بفوترة بنود الإرجاع على الفور.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">لتوفير رؤية أفضل لمختلف المبالغ في سلة التسوق، تمت إضافة ثلاثة حقول مبالغ جديدة إلى سلة التسوق.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>You can use the screen designer to make these new fields available in the POS user interface (UI).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ويمكنك استخدام مصمم الشاشة لجعل كافة هذه الحقول الجديدة متوفرة في واجهة مستخدم (UI) نقطة البيع.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Deposit applied<ept id="p1">**</ept> – The deposit amount that is applied on a transaction when the user does a customer order pickup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>‏‫تم استخدام الإيداع‬<ept id="p1">**</ept> – مبلغ الإيداع المطبق على حركة عندما يقوم المستخدم بانتقاء أمر العميل‬.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">إذا لم يكن هناك أي مبلغ تجاوز الإيداع، وإذا تم تكوين إيداع بنسبة 10 بالمئة، سيكون المبلغ في هذا الحقل 90 بالمئة من المبلغ الإجمالي لأمر العميل.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>Carry out amount<ept id="p1">**</ept> – The total amount for lines where the delivery mode was set to <bpt id="p2">**</bpt>Carry out<ept id="p2">**</ept> when the customer order was created or edited, or during a customer order exchange.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>تنفيذ المبلغ<ept id="p1">**</ept> – المبلغ الإجمالي للبنود حيث تم تعيين وضع التسليم إلى <bpt id="p2">**</bpt>تنفيذ<ept id="p2">**</ept> عندما تم إنشاء أمر العميل أو تحريره، أو خلال استبدال أمر العميل.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The amount in this field includes taxes and charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">يتضمن المبلغ الموجود في هذا الحقل الضرائب والمصاريف.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Return amount<ept id="p1">**</ept> – The total amount for lines that have negative quantities during the customer order exchange.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>المبلغ المرتجع‬<ept id="p1">**</ept> – المبلغ الإجمالي للبنود ذات الكميات السالبة أثناء استبدال أمر العميل.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The amount in this field includes taxes and charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">يتضمن المبلغ الموجود في هذا الحقل الضرائب والمصاريف.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>