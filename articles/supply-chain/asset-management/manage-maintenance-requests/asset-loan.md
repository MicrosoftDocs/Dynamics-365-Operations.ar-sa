---
title: الأصول المقترضة
description: يشرح هذا الموضوع كيفية تسجيل الأصول المقترضة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d76d8e9b735adc1fa796cff5e0ef7d049d109144
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253436"
---
# <a name="asset-loans"></a><span data-ttu-id="b8574-103">الأصول المقترضة</span><span class="sxs-lookup"><span data-stu-id="b8574-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b8574-104">إذا كانت شركتك تتلقي أصولاً لمهام إصلاح أو صيانة من مواقع داخلية أو عملاء، وإذا قمت مؤخرًا بإقراض الأصول إلى هذه المواقع أو هؤلاء العملاء، فبإمكان إدارة الأصول تعقب الأصول المقترضة.</span><span class="sxs-lookup"><span data-stu-id="b8574-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="b8574-105">تسجيل الأصول المقترضة في طلب صيانة</span><span class="sxs-lookup"><span data-stu-id="b8574-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="b8574-106">حدد **إدارة الأصول** \> **عام** \> **طلبات الصيانة** \> **جميع طلبات الصيانة** أو **طلبات الصيانة النشطة**.</span><span class="sxs-lookup"><span data-stu-id="b8574-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="b8574-107">حدد طلب الصيانة لتسجيل الأصل المقترض عليه، ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="b8574-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="b8574-108">في صفحة **الطلب**، حدد **إرسال الأصل المقترض**.</span><span class="sxs-lookup"><span data-stu-id="b8574-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="b8574-109">حدد الأصل، ثم ادخل تاريخ الإرجاع المتوقع.</span><span class="sxs-lookup"><span data-stu-id="b8574-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="b8574-110">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b8574-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="b8574-111">يمكنك إرسال أصل مقترض فقط إذا توفر لديك أصل من نوع الأصل نفسه.</span><span class="sxs-lookup"><span data-stu-id="b8574-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="b8574-112">يجب أن يكون للأصل المقترض حالة دورة حياة أصل تسمح باستخدامه كـصل مقترض، مثل **InStorage**.</span><span class="sxs-lookup"><span data-stu-id="b8574-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="b8574-113">عند تسجيل الأصل المقترض، يتم تلقائيًا تحديث حالة دورة حياة الأصل الخاصة بالأصل بشكل تلقائي إلى، على سبيل المثال، **OnLoan**.</span><span class="sxs-lookup"><span data-stu-id="b8574-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="b8574-114">لعرض قائمة بكافة الأصول التي قمت بإقراضها إلى مواقع أو عملاء آخرين، حدد **إدارة الأصول** \> **عام** \> **أصل مقترض** \> **جميع الأصول المقترضة**.</span><span class="sxs-lookup"><span data-stu-id="b8574-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="b8574-115">إذا كانت خانة الاختيار **منتهٍ** لأحد الأصول محددة، فهذا يعني أنه تم تسجيل الأصل كما تم إرجاعه إلى شركتك.</span><span class="sxs-lookup"><span data-stu-id="b8574-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![إدارة طلبات الصيانة](media/06-manage-maintenance-requests.png)

<span data-ttu-id="b8574-117">في صفحة **الأصول المقترضة النشطة**، يمكنك عرض قائمة بجميع الأصول المقترضة التي لم يتم إرجاعها بعد إلى شركتك.</span><span class="sxs-lookup"><span data-stu-id="b8574-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="b8574-118">تسجيل الأصول المقترضة كمرتجعة</span><span class="sxs-lookup"><span data-stu-id="b8574-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="b8574-119">حدد **إدارة الأصول** \> **عام** \> **أصل مقترض** \> **الأصول‏‎ المقترضة النشطة**.</span><span class="sxs-lookup"><span data-stu-id="b8574-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="b8574-120">حدد الأصل المقترض لتسجيله كمرتجع، ثم حدد **إرجاع الأصل المقترض**.</span><span class="sxs-lookup"><span data-stu-id="b8574-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="b8574-121">في الحقل **مُرتجع‬**، أدخل التاريخ والوقت.</span><span class="sxs-lookup"><span data-stu-id="b8574-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="b8574-122">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b8574-122">Select **OK**.</span></span>
5. <span data-ttu-id="b8574-123">قم بتحديث صفحة **الأصول المقترضة النشطة**، ولاحظ عدم ظهور الأصل المقترض في القائمة.</span><span class="sxs-lookup"><span data-stu-id="b8574-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]