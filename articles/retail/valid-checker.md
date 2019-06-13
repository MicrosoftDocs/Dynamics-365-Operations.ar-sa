<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="valid-checker.md" target-language="ar-SA">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>valid-checker.125a66.1fc894206f9d90fce1e2eab292ac241e9d943e23.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1fc894206f9d90fce1e2eab292ac241e9d943e23</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\valid-checker.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">مدقق تناسق حركة البيع بالتجزئة</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the retail transaction consistency checker functionality in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">يصف هذا الموضوع وظيفة مدقق تناسق حركة البيع بالتجزئة في Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">مدقق تناسق حركة البيع بالتجزئة</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">يصف هذا الموضوع وظيفة مدقق تناسق حركة البيع بالتجزئة في Microsoft Dynamics 365 for Finance and Operations ، الإصدار 8.1.3.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">يحدد مدقق التناسق الحركات غير المتناسقة ويعزلها قبل انتقائها من قبل عملية ترحيل كشف الحساب.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When a statement is posted in Microsoft Dynamics 365 for Retail, posting can fail due to inconsistent data in the retail transaction tables.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">عند ترحيل كشف حساب في Microsoft Dynamics 365 for Retail، قد يفشل الترحيل بسبب وجود بيانات غير متناسقة في جداول حركات البيع بالتجزئة.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The data issue may be caused by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">قد يعود سبب المشكلة في البيانات إلى ظهور مشاكل غير متوقعة في تطبيق نقطة البيع (POS)، أو إذا تم استيراد الحركات بشكل غير صحيح من أنظمة نقطة البيع الخارجية.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Examples of how these inconsistencies may appear include:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">تشتمل الأمثلة حول كيفية ظهور حالات عدم التناسق هذه على ما يلي:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The transaction total on the header table does not match the transaction total on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">إجمالي الحركة في جدول الرأس غير متطابق مع إجمالي الحركة في البنود.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The line count on the header table does not match with the number of lines in the transaction table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">عدد البنود في جدول الرأس غير متطابق مع عدد البنود في جدول الحركة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Taxes on the header table do not match the tax amount on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">الضرائب في جدول الرأس غير متطابقة مع قيمة الضريبة في البنود.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">عندما تنتقي عمليات ترحيل كشوف الحسابات حركات غير متناسقة، يتم إنشاء دفاتر يومية دفعات وفواتير مبيعات غير متناسقة، وتفشل عملية ترحيل كشف الحساب بكاملها نتيجة لذلك.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">تشتمل عملية استرداد كشوف الحسابات من حالة من هذا النوع على عمليات إصلاح معقدة للبيانات عبر جداول حركات متعددة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The retail transaction consistency checker prevents such issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">يمنع مدقق تناسق حركة البيع بالتجزئة حدوث مثل هذه المشاكل.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The following chart illustrates the posting process with the transaction consistency checker.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">يوضح المخطط التالي عملية الترحيل باستخدام مدقق تناسق الحركة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">![</bpt>Statement posting process with retail transaction consistency checker<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Statement posting process with retail transaction consistency checker<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>عملية ترحيل كشف الحساب باستخدام مدقق تناسق حركة البيع بالتجزئة<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>عملية ترحيل كشف الحساب باستخدام مدقق تناسق حركة البيع بالتجزئة<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The <bpt id="p1">**</bpt>Validate store transactions<ept id="p1">**</ept> batch process checks the consistency of the retail transaction tables for the following scenarios.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">تدقق العملية الدُفعية <bpt id="p1">**</bpt>التحقق من صحة حركات المتجر‬<ept id="p1">**</ept> في تناسق جداول حركات البيع بالتجزئة للسيناريوهات التالية.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Customer account<ept id="p1">**</ept> – Validates that the customer account in the retail transaction tables exists in the HQ customer master.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>حساب العميل<ept id="p1">**</ept> – التأكد من أن حساب العميل في جداول حركات البيع بالتجزئة موجود في المقر الرئيسي للعميل.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Line count<ept id="p1">**</ept> – Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>عدد البنود<ept id="p1">**</ept> – التأكد من أن عدد البنود، كما تم تسجيله في جدول رأس الحركة، يتطابق مع أرقام البنود في جداول حركة مبيعات.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Price includes tax<ept id="p1">**</ept> – Validates that the <bpt id="p2">**</bpt>Price includes tax<ept id="p2">**</ept> parameter is consistent across transaction lines.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>السعر يشمل الضريبة<ept id="p1">**</ept> – التأكد من أن المعلمة <bpt id="p2">**</bpt>السعر يشمل الضريبة<ept id="p2">**</ept> متناسقة عبر بنود الحركة.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>Gross amount<ept id="p1">**</ept> – Validates that the gross amount on the header is the sum of the net amounts on the lines plus the tax amount.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>إجمالي المبلغ<ept id="p1">**</ept> – التأكد من ان إجمالي المبلغ في الرأس هو مجموع المبالغ الصافية الموجودة في البنود بالإضافة إلى مبلغ الضريبة.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Net amount<ept id="p1">**</ept> – Validates that the net amount on the header is the sum of the net amounts on the lines.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>المبلع الصافي<ept id="p1">**</ept> – التأكد من ان المبلغ الصافي‏‎ في الرأس هو مجموع المبالغ الصافية الموجودة في البنود بالإضافة إلى مبلغ الضريبة.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Under / Over payment<ept id="p1">**</ept> – Validates that the difference between the gross amount on the header and the payment amount doesn't exceed the maximum underpayment/overpayment configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>دفع بالزيادة/بالنقصان‬<ept id="p1">**</ept> – التأكد من أن الفرق بين إجمالي المبلغ على الرأس ومبلغ الدفع لا يتجاوز تكوين دفع بالزيادة/بالنقصان.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Discount amount<ept id="p1">**</ept> – Validates that the discount amount on the discount tables and the discount amount on the retail transaction line tables are consistent, and that the discount amount on the header is the sum of the discount amounts on the lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>مبلغ الخصم<ept id="p1">**</ept> – التأكد من تناسق مبلغ الخصم في جداول الخصم ومبلغ الخصم في جداول بنود حركة البيع بالتجزئة، وأن مبلغ الخصم في الرأس هو مجموع مبالغ الخصم في البنود.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Line discount<ept id="p1">**</ept> – Validates that the line discount on the transaction line is the sum of all the lines in the discount table that corresponds to the transaction line.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>خصم البند<ept id="p1">**</ept> – التأكد من أن خصم البند على بند الحركة هو مجموع كافة البنود في جدول الخصم الذي يتوافق مع بند الحركة.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Gift card item<ept id="p1">**</ept> – Retail doesn't support the return of gift card items.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>صنف بطاقة الهدايا‬<ept id="p1">**</ept> – لا يدعم Retail إرجاع أصناف بطاقة الهدايا.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>However, the balance on a gift card can be cashed out. Any gift card item that is processed as a return line instead of a cash-out line fails the statement posting process.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ومع ذلك، يمكن صرف الرصيد في بطاقة الهدايا. عند معالجة صنف بطاقة هدايا كبند مرتجع بدلاً من بند مصروف، فهو يفشل في عملية ترحيل كشوف الحسابات.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The validation process for gift card items helps guarantee that the only return gift card line items on the retail transaction tables are gift card cash-out lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">تضمن عملية التحقق من الصحة التي تتم على أصناف بطاقة الهدايا أن تكون فقط عناصر بنود بطاقة الهدايا المرتجعة على جداول حركة البيع بالتجزئة البنود المصروفة في بطاقة الهدايا.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Negative price<ept id="p1">**</ept> – Validates that there are no negative price transaction lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>السعر السالب<ept id="p1">**</ept> – يتحقق من عدم وجود بنود حركة ذات سعر سالب.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Item &amp; Variant<ept id="p1">**</ept> – Validates that items and variants on the transaction lines exist in the item and variant master file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>الصنف والمتغير<ept id="p1">**</ept> – التأكد من أن الأصناف والمتغيرات في بنود الحركة موجودة في الملف الرئيسي للصنف والمتغير.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Set up the consistency checker</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">إعداد مدقق التناسق</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Configure the "Validate store transactions" batch process, at <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> POS posting<ept id="p1">**</ept>, for periodic runs.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">قم بتكوين العملية الدُفعية "التحقق من صحة حركات المتجر‬" في <bpt id="p1">**</bpt>البيع بالتجزئة <ph id="ph1">\&gt;</ph> تكنولوجيا معلومات البيع بالتجزئة‬ <ph id="ph2">\&gt;</ph> ترحيل نقطة البيع<ept id="p1">**</ept>، لعمليات التشغيل الدورية.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">يمكن جدولة الوظيفة الدُفعية استنادًا إلى التدرج الهرمي للمؤسسات في المتجر، بطريقة مماثلة لكيفية إعداد العمليتين "حساب الكشوف على دُفعات‬" و"ترحيل الكشوف على دُفعات‬".</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">من المستحسن تكوين هذه العملية الدُفعية لتشغيلها عدة مرات في اليوم وجدولتها بحيث يتم تشغيلها في نهاية كل تنفيذ لوظيفة P.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Results of validation process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">نتائج التحقق من الصحة</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The results of the validation check by the batch process are tagged on the appropriate retail transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">توضع علامة نتائج التحقق من الصحة التي تقوم بها العملية الدُفعية على حركة البيع بالتجزئة المناسبة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The <bpt id="p1">**</bpt>Validation status<ept id="p1">**</ept> field on the retail transaction record is either set to <bpt id="p2">**</bpt>Successful<ept id="p2">**</ept> or <bpt id="p3">**</bpt>Error<ept id="p3">**</ept>, and the date of the last validation run appears on the <bpt id="p4">**</bpt>Last validation time<ept id="p4">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">يكون الحقل <bpt id="p1">**</bpt>حالة التحقق من الصحة<ept id="p1">**</ept> على سجل حركة البيع بالتجزئة معينًا إلى <bpt id="p2">**</bpt>ناجح‬<ept id="p2">**</ept> أو <bpt id="p3">**</bpt>خطأ<ept id="p3">**</ept>، ويظهر تاريخ تشغيل عملية التحقق من الصحة الأخيرة في الحقل <bpt id="p4">**</bpt>وقت آخر عملية تحقق من الصحة<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the <bpt id="p1">**</bpt>Validation errors<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">لعرض نص وصفي للخطأ المتعلق بفشل التحقق من الصحة، حدد سجل حركة متجر البيع بالتجزئة الملائم، ثم انقر فوق الزر <bpt id="p1">**</bpt>أخطاء التحقق من الصحة<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">لن تتضمن كشوف الحسابات الحركات التي لم تنجح في عملية التحقق من الصحة والحركات التي لم يتم بعد التحقق من صحتها.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">أثناء عملية "حساب كشف الحساب"، سيتم يتم إبلاغ المستخدمين عن وجود حركات كان يجب تضمينها في كشف الحساب ولكن لم يتم تضمينها فيه.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If a validation error is found, the only way to fix the error is to contact Microsoft Support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">إذا تم العثور على خطأ يتعلق بالتحقق من الصحة، فإن الطريقة الوحيدة لإصلاحه هو الاتصال بدعم Microsoft.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In a future release, capability will be added so that users can fix the records that failed through the user interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">في إصدار مستقبلي، سنضيف ميزة تسمح للمستخدمين بإصلاح السجلات التي فشلت عبر واجهة المستخدم.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Logging and auditing capabilities will also be made available to trace the history of the modifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">وسنوفر أيضًا قدرات التسجيل والتدقيق لتتبع محفوظات التعديلات.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Additional validation rules to support more scenarios will be added in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">سنضيف المزيد من قواعد التحقق من الصحة لدعم سيناريوهات إضافية في إصدار مستقبلي.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>