---
title: تعيين معلمات TDS في الحسابات الدائنة والحسابات المدينة
description: يوضح هذا الموضوع كيفية تعيين المعلمات في الحسابات الدائنة والحسابات المدينة لدعم ضريبة الخصم في المصدر (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022998"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="885ed-103">تعيين معلمات TDS في الحسابات الدائنة والحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="885ed-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="885ed-104">يوضح هذا الموضوع كيفية تعيين المعلمات في الحسابات الدائنة والحسابات المدينة لدعم ضريبة الخصم في المصدر (TDS).</span><span class="sxs-lookup"><span data-stu-id="885ed-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="885ed-105">انتقل إلى **الضريبة \> إعداد \> المعلمات \> معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="885ed-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="885ed-106">في علامة التبويب **تحديثات**، حدد **تحديث بنود الأمر** لفتح مربع الحوار **تحديث بنود الأوامر**.</span><span class="sxs-lookup"><span data-stu-id="885ed-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="885ed-107">في القسم **مجموعة TDS**، في الحقل **تحديث مجموعة TDS**، حدد الأسلوب الذي سيتم استخدامه لتحديث مجموعة TDS على مستوى البند.</span><span class="sxs-lookup"><span data-stu-id="885ed-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="885ed-108">يستخدم هذا الإعداد عند تحديث المجموعة TDS في رأس الأمر.</span><span class="sxs-lookup"><span data-stu-id="885ed-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="885ed-109">وتتوفر الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="885ed-109">The following options are available:</span></span>

    - <span data-ttu-id="885ed-110">**أبدًا** – لا يتم تحديث مجموعة TDS في بنود الأمر عند تحديثها في رأس الأمر.</span><span class="sxs-lookup"><span data-stu-id="885ed-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="885ed-111">**دائمًا** – يتم تحديث مجموعة TDS تلقائيًا في بنود الأمر عند تحديثها في رأس الأمر.</span><span class="sxs-lookup"><span data-stu-id="885ed-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="885ed-112">**المطالبة** – يتلقى المستخدمون رسالة تطالبهم بتحديث مجموعة TDS في بنود الأمر.</span><span class="sxs-lookup"><span data-stu-id="885ed-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="885ed-113">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="885ed-113">Select **OK**.</span></span>

    <span data-ttu-id="885ed-114">[![مربع الحوار تحديث بنود الأمر](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="885ed-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="885ed-115">انتقل إلى **الضريبة \> إعداد \> المعلمات \> معلمات الحسابات الدائنة**.</span><span class="sxs-lookup"><span data-stu-id="885ed-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="885ed-116">في علامة التبويب **عام**، على علامة التبويب السريعة  **التقسيم استنادًا إلى معلومات التسليم**، قم بتعيين الخيار **إيصال استلام المنتجات** على **نعم** لترحيل إيصال استلام المنتجات الذي يحتوي على عناوين تسليم وأرقام حساب الضرائب المختلفة (TAN) وتقسيمها.</span><span class="sxs-lookup"><span data-stu-id="885ed-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="885ed-117">إذا تم تعيين هذا الخيار إلى **لا**، فإنه لا يمكنك ترحيل إيصال تعبئة مشتريات يحتوي على عناوين تسليم وأرقام TAN مختلفة.</span><span class="sxs-lookup"><span data-stu-id="885ed-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="885ed-118">قم بتعيين الخيار **الفاتورة** على **نعم** لترحيل فاتورة الشراء التي لها عناوين تسليم وأرقام TAN مختلفة وتقسيمها.</span><span class="sxs-lookup"><span data-stu-id="885ed-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="885ed-119">[![علامة التبويب السريعة التقسيم استنادًا إلى معلومات التسليم](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="885ed-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="885ed-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="885ed-120">Close the page.</span></span>
